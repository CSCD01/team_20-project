# Requiremnt
## [Issue#16482](https://github.com/matplotlib/matplotlib/issues/13799) (API Consistency)
Currently the **hlines** and **vlines** function in **pyplot** (script layer) default the color for lines to black. However, the issuer showed a scenario that it is better for the default color to be same as what is set in rcParams.\

>hlines and vlines color does not default to lines.color in rcParams. The default argument is 'k' which doesn't work with dark backgrounds.
##### Code for reproduction
```python
import matplotlib.pyplot as plt
import matplotlib as mpl
plt.style.use('dark_background')

plt.figure()
with mpl.rc_context({'lines.color':'white'}):
   plt.hlines(0.5, 0, 1) # defaults to a black line, which doesn't work with a dark background
   plt.vlines(0.5, 0, 1, colors=None) # This will fall back to `lines.color`
```

## Expected outcome
If the color property for **hlines** and **vlines** is not provided, then default the color to lines.color in rcParams.