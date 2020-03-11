# Issue List Report

[Initial Bug Report](https://github.com/CSCD01/team_20-project/blob/master/deliverables/2/Initial_Bug_Fixes_Report.pdf)

# Issue Choice Report

## [Issue 13799](https://github.com/matplotlib/matplotlib/issues/13799)

### Argument
First of all, this bug is not easy or too hard. This bug requires a large amount of understanding of the basic flow in matplotlib as well as the numpy stack. We have to figure out how the NaN value is rendered or passed between different objects. Second, this bug has been confirmed by the core contributors of Matplotlib -- that Errorbar is not supposed to ignore the invalid point and shift the colour to the next valid point. Furthermore, there is only one team who previously worked on this bug, and their submitted PR was rejected due to incorrect implementation and no further updates were made since March 2019.

### Estimate
Need to modify the way Errorbars object handles NaN values. The correct fix is keeping all of the NaN values instead of removing them from the axis. The previous PR was rejected because the author simply removed the corresponding colour of invalid points before passing values to Errorbar object. The Estimated time is 5 hours, which includes 2 hours for tracing and analyzing, 1 hour for implementation, 1 hour for testing, and 1 hour for reviewing and submitting the PR.

### Risk
The risk can be found in how Matplotlib handles NaN values. If Matplotlib does not support NaN values in the Axis object and always removes the NaN values instead of keeping them as invalid points, then the correct fix of the bug possibly involves changing the structure of the dependencies of many objects in Matplolib, which is out of range for this task. 


## [Issue 16389](https://github.com/CSCD01/team_20-project/tree/master/deliverables/2/matplotlib%2316389)

### Argument
By implementing this fix it would help familiarize ourselves with the core process of creating artist inherited objects within mathplotlib. This will help us better understand the system as well as it looks like a good first issue which can be resolved and even merged within the given timeframe of the deliverable.

### Estimate
The effort in fixing this bug would be an estimated three hours. An hour and a half would be used for completing documentation and analysis. A great deal of this would be taken up by code tracing in order to properly locate and plan where the fix should occur. The second half of this estimate will be the quick implementation of the plan, the creating of a test for this specific bug case, as well as submitting a pull request. 

### Risk
The risk which can be found in how this bug fix is implemented. Our decided fix for fontProperties could conflict with the lead contributor's perspective on, at which specific level of the code the fix should be put into place. Another risk can come from us modifying the way in which labels are read to ensure this bug is fixed, but in the process breaking another aspect of Text.

## [Issue 16482](https://github.com/matplotlib/matplotlib/issues/13799)

### Argument
This issue should be a simple fix, and involves fundamental usage of matplotlib. We probably will need to trace the code through different layers. It's a good start point to get familiar with matplolib porject and the process of contributing to open source projects. 
### Estimate
The issue it self should not take too much time to fix. The approximation will be 1 hour on trace through the code and 1 hour to make the fix. However, since its the first time we work on the open source project, we need to read through the relevant document including the contribution process and the tools involved during developing. The approximation of reading through documents is about 2 hours, 1 hour on setting up the development environment of the project, and 1 hour on getting familiar with the relevant tools for the project (ie. pytest). In conclusion, the estimation for this issue is 6-10 hours.
### Risk
THe risk for fixing this bug could be how the bug is actually triggered. Since issuer stated that the color should be default to the settings in rcParam, how the rcParam is implemented may affect the complexity of the issue. 

# Gantt Chart for estimated work for each phase
![alt text](https://github.com/CSCD01/team_20-project/blob/master/deliverables/2/GanttChart.PNG "Deliverable 2 Gantt Chart")