# User Guide

## How to Use
This feature will be placed accessible in the outermost wrapper of matplotlib as a method used from pyplot. In order to use this methods, two prerequisites exist; a line graph must be used for a usable result from labeled lines, and the method is called after the creation of the graph. To use this method simply use the imported pyplot module which is regularly imported as plt, and call plt.label_lines().  

## When to Use This Feature
While this feature can be used for any labeled line graphs, there are good and bad situations for it to be used in. For instance, a graph in which all lines approach a single value such as 0 or 100% would be fairly useless as all of the labels would be clumped together. This is not to say the graph must be sparse as the majority of graphs would be represented very well with the use of line_labels automatic spacing. Even a very densely spaced graph would be a good candidate for this method as it scales well when the client makes use of the zoom tool. This allows for enough space for all the labels and a quick reference point when considering sections of the graph rather than going between the graph and legend. Overall this is a very versatile tool for line graphs and will provide a very good experience for the majority of use cases.
