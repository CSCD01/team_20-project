# [Pull Request](https://github.com/matplotlib/matplotlib/pull/16694)

Changes to the codebase as well as the test added to the test suite can be found under the submitted pull request.

# Test Cases

Due to the nature of this bug it was found that a single simple test was required in order to check if proper priority occurs with the fontProperties lable. Combined with the existing test suite this would be sufficient to check if the bug no longer affects mathplotlib, and nothing was broken in the process.

# Commentary

This only affected source code file was the Text.py. A quick check is done for fontProperties in order to give it priority and pop it our of the dictionary before continuing on with the normally followed process. This does little to affect the design of the code. 