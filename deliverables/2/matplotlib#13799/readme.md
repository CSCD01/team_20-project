# [Pull Request](https://github.com/matplotlib/matplotlib/pull/16724)

The results of the development and Testing phase can both be found under the pull request which acts the release phase.

# Test Cases
Test cases is focusing on if `Hlines` and `Vlines` object having the correct behavior after modification. Matplotlib provides many advanced functionality test for `Hlines` and `Vlines`, our fix passed all the functionality test. Furthermore, we added some test cases to test if `Hlines` or `Vlines` can work properly with variable colour and Nan value. We created `test_vlines_with_nan_colors`, `test_vlines_with_masked_colors`, `test_hlines_with_nan_colors`, `test_hlines_with_masked_colors` cases.

Each test case is using `check_figures_equal()` to compare the colours of Hlines and Vlines with Nan value and non-Nan value.

For example:
``` 
# fig_test and fig_ref shou be exactly same
# More details of the code can be found in PR lib/matplotlib/tests/test_axes.py.   
colors1 = ['red', 'green', 'blue', 'purple', 'orange', 'black']
x1 = [2, 3, 4, 5, 6, 7]
y1 = [2, -6, 3, 8, np.nan, 2]

fig_test, ax1 = plt.subplots()
ax1.vlines(y1, 0, x1, colors=colors1, linewidth=5)

colors2 = ['red', 'green', 'blue', 'purple', 'black']
x2 = [2, 3, 4, 5, 7]
y2 = [2, -6, 3, 8, 2]
# Reference image
fig_ref, ax2 = plt.subplots()
ax2.vlines(y2, 0, x2, colors=colors2, linewidth=5)
```

# Commentary
This fix only affect the `Hlines` and `Vlines` function in `_axes.py`. Now the `Hlines` and `Vlines` keeps the invalid points instead of removing them and pass the point as Masked Array to `LineCollection`. Since this is an inconsistency issue that 'LineCollection' already supports to accept Masked Array input and detect invalid points, it is not necessary to change any code in `LineCoolection` or the other objects.
