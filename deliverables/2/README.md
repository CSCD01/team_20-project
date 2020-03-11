# Issue List Report

[Initial Bug Report](https://github.com/CSCD01/team_20-project/blob/master/deliverables/2/Initial_Bug_Fixes_Report.pdf)

# Issue Choice Report

## Issue 13799

### Argument
First of all, this bug is not easy or too hard. This bug requires a large amount of understanding of the basic process in matplotlib. We have to figure out how the Nan value is drawed or passed between different objects. Second, the bug has been confirmed with Matplotlib, that Errorbar is not supposed to ignore the invalid point and shift the colour to the next valid point. Furthermore, there is only one team working on this bug, but the submitted PR was rejected due to incorrect implementation and no further update since March 2019.

### Estimate

### Risk

## [Issue 16389](https://github.com/CSCD01/team_20-project/tree/master/deliverables/2/matplotlib%2316389)

### Argument
By implementing this fix it would help familiarize ourselves with the core process of creating artist inherited objects within mathplotlib. This will help us better understand the system as well as it looks like a good first issue which can be resolved and even merged within the given timeframe of the deliverable.

### Estimate
The effort in fixing this bug would be an estimated three hours. An hour and a half would be used for completing documentation and analysis. A great deal of this would be taken up by code tracing in order to properly locate and plan where the fix should occur. The second half of this estimate will be the quick implementation of the plan, the creating of a test for this specific bug case, as well as submitting a pull request. 

### Risk
The risk which can be found in how this bug fix is implemented. Our decided fix for fontProperties could conflict with the lead contributor�s perspective on, at which specific level of the code the fix should be put into place. Another risk can come from us modifying the way in which labels are read to ensure this bug is fixed, but in the process breaking another aspect of Text.

## Issue 16482

### Argument

### Estimate

### Risk
