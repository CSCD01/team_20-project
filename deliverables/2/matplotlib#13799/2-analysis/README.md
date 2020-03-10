# Analysis
## Summary
After analyzing the codebase, the inconsistency issue was traced to the difference between the handling of NaN values in `Axis.scatter` versus `Axis.hlines`/`Axis.vlines`. In the latter case, NaN values were being deleted from their respective `np.array`, whereas in the former case, NaN values were handled by using a `np.ma.array` (masked array), where the NaN values were simply masked. To keep the behaviour consistent with the core contributors' goals, the implemented bugfix modifies both `Axis.hlines` and `Axis.vlines` methods to store the input as a masked array rather than deleting NaN (or masked) values.
## Files
### _axes.py
#### hlines() and vlines()
##### Problem
* `cbook.delete_masked_points()` was deleting points from the dataset, a behaviour which is inconsistent to `Axis.scatter`.
##### Solution
* No longer use `cbook.delete_masked_points()`.
* `cbook._combine_masks()` allowed for the masking of all points where there exists a NaN value (across multiple arrays).
* Data must now be stored as a `np.ma.array` rather than a `np.array` since we are dealing with masked values.