# User Guide

## How to Use
This feature will be made accessible in the outermost wrapper of matplotlib as a method inside of `pyplot`. In order to use this method, two prerequisites exist: a line graph must be used for a usable result from `label_lines`, and the method is called after the creation of the graph. To use this method, simply use the imported `pyplot` module which is regularly imported as `plt`, and call `plt.label_lines()`.  

## When to Use This Feature
While this feature can be used for any labelled line graphs, there are evidently good and bad situations in which it can be used. For instance, a graph for which all lines approach a single value, such as 0 or 100%, would be fairly useless as all of the labels would be clumped together. This is not to say the graph must be sparse, as the majority of graphs would be represented very well with the use of the automatic spacing implemented by `line_labels` . Even a very densely spaced graph would be a good candidate for this method, as it scales well when the client makes use of the zoom tool. This allows for enough space for all the labels and a quick reference point when considering sections of the graph, rather than going between the graph and legend. Overall this is a very versatile tool for line graphs and will provide a very good experience for the majority of use cases.
