# Analysis
## Summary
After analyzing the codebase, there are two places need to change. The default color is set to 'k' in both file **pyplot.py** and **_axes.py**. Later when adding the lines in **collections.py**, it checks if the **colors** property is **None**, if its None then the collors of thel lines will default to lines.colors in rcParam. In this case, since the default colors of **hlines** and **vlines** is already set to 'k', so it will not set to lines.colors.

## Files
### pyplot.py
#### hlines() and vlines()
##### Problem
* `def hlines(self, y, xmin, xmax, colors='k', linestyles='solid',
               label='', **kwargs)` and `def vlines(self, y, xmin, xmax, colors='k', linestyles='solid',
               label='', **kwargs)`default the colors to 'k'

### \_axes.py
#### hlines() and vlines()
##### Problem
* `def hlines(self, y, xmin, xmax, colors='k', linestyles='solid',
               label='', **kwargs):` and `def vlines(self, y, xmin, xmax, colors='k', linestyles='solid',
               label='', **kwargs)` default the colors to 'k'
## Solution
* default **colors** property to **None** for **hlines** and **vlines** when it's not provided.