## Acceptance Test
The feature that the user wants is to label the lines near the end of each line. An example result from user's posting will be like\
![user example](./userExample.png)\
Our acceptance tests contain a set of line graphs, before the implementation, they are labeled using the _legend()_ function. After the implementation, the graphs should have their label at the end of each line.
### Real world statistic graphs scenarios
#### How much food can you buy for working one hour in the manufacturing sector
Using _legend()_ function:
![how_much_food_lengend](./how_much_food_lengend.png)\

#### Domestic food price volatility index
Using _legend()_ function:
![domestic_food_price_legend](./domestic_food_price_legend.png)\

#### COVID19 data on second half of month March
Using _legend()_ function:
![covid19_legend](./covid19_legend.png)\

#### Commodity price index of cereal crops and petroleum 1850 2015
Using _legend()_ function:
![commodity_price_index_legend](./commodity_price_index_legend.png)\

#### Percent bachelors degrees women USA
Using _legend()_ function:
![degree_legend](./degree_legend.png)\

### Tests for edge cases graphs scenarios
#### All lines ends at close points
Using _legend()_ function:
![one_point_graph_legend](./one_point_graph_legend.png)\

#### Lines ends at different close points
Using _legend()_ function:
![group_point_graph_legend](./group_point_graph_legend.png)\



## Acceptance Test Result
After the implementation of our feature, users will be able to label the lines at the end of each line in a decent way.\
Instead of _lengend()_, users will call the newly implemented function _label_lines()_. The function will place the line labels at the end of each line in a responsive manner. Users can zoom the graph to get a decent label position for lines ends at close points. By running the test cases above using the _label_lines()_ function, the following graphs are produced.
### Real world statistic graphs scenarios
#### How much food can you buy for working one hour in the manufacturing sector
Using _label_lines()_ feature:
![how_much_food_label](./how_much_food_label.png)\

#### Domestic food price volatility index
Using _label_lines()_ feature:
![domestic_food_price_label](./domestic_food_price_label.png)\
When the graph contains a lot of lines, our feature will try to group labels for lines that have similar end points. Users can zoom into the graph and the labels position will update accordingly. After zoom into the above messy graph, we will get a better labeled graph as follow.
![domestic_food_price_label_zoom](./domestic_food_price_label_zoom.png)\
With further zoom in, the labels can be clearly showed. 
![domestic_food_price_label_zoommore](./domestic_food_price_label_zoommore.png)\

#### COVID19 data on second half of month March
Using _label_lines()_ feature:
![covid19_label](./covid19_label.png)\

#### Commodity price index of cereal crops and petroleum 1850 2015
Using _label_lines()_ feature:
![commodity_price_index_label](./commodity_price_index_label.png)\

#### Percent bachelors degrees women USA
Using _label_lines()_ feature:
![degree_label](./degree_label.png)\

### Tests for edge cases graphs scenarios

#### All lines ends at close points
Using _label_lines()_ feature:
![one_point_graph_label](./one_point_graph_label.png)\
After zoom into the end points of the lines:\
![one_point_graph_label_zoom](./one_point_graph_label_zoom.png)\

#### Lines ends at different close points
Using _label_lines()_ feature:
![group_point_graph_label](./group_point_graph_label.png)\
After zoom into the end points of the lines:\
![group_point_graph_label_zoom](./group_point_graph_label_zoom.png)\
Further zoom until the label is clear:\
![group_point_graph_label_zoommore](./group_point_graph_label_zoommore.png)\

#### Max number of labels
The max number of labels can be shown in a graph:\
![bucket_fill](./bucket_fill.png)\
#### Label density
Labels when lines end at the same point:\
![bucket_density](./bucket_density.png)\

