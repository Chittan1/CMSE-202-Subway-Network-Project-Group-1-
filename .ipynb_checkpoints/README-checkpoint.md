# CMSE-202-Subway-Network-Project-Group-1-

## Question: What is the most efficient way to connect the United States' major cities by train?

We used a dataset of the top 1,000 U.S. cities in order to represent the geographic relationship between them. Our dataset is from GitHub at https://github.com/plotly/datasets/blob/master/us-cities-top-1k.csv.

To run our code, you need to download the dataset and all the packages used (pandas, numpy, networkx, and matplotlib). When you run the code, it starts by loading in the dataset of the U.S. cities, and then filters out Alaska and Hawaii because it's not practical to connect those to the other states by subway and/or train. Then, we select the top 100 cities by population and build a base graph of all the nodes. Then we take it one step further and ensure there is only one node (city) per state.

Next, we created multiple network models to compare different ways to connect the cities. There is the nearest neighbors model, the distance threshold model, the minimum spanning tree model, and a hybrid model of the neighbors and minimum spanning tree. Finally, we analyzed the route efficiency between the major city pairs, created a model comparison summary, and a final ranking of the models.

## Group Contributions

Maggie loaded all of our packages and data. She also cleaned all the data and filtered it to exclude Hawaii and Alaska. Finally, she built the two base graphs with nodes for us to use, one of the top 100 U.S. cities and one with one node in each state. 

Hanna created and evaluated two models. One is the nearest neighbors model, which connects each node to its three closest neighbors. The other is the distance-threshold model, which connects each city only if they are within 475 km of each other.

Anwith also created and evaluated some models. The first was the minimum spanning tree model, which finds the cheapest way to connect all the cities and uses the smallest total distance possible. Next was the hybrid model, which was first connected each city to its three closest cities, but then he expanded on this model by adding a minimum spanning tree to it as well. Finally, he made the state-based neighboring graph. This one used the base graph that Maggie made with one node in each state and then connected each state to its three nearest states.

Ariadna then compared our models to test which one was most efficient by checking how well each one connected specific pairs that are heavily traveled, like Detroit to Chicago, or L.A. to San Francisco.

Finally, Frankie, instead of measuring each model, he ranked them overall based on lots of criteria. He compared the models created by Hanna and Anwith using average efficiency, connectivity, cost, and robustness. Then, he combined it all into a final score to rank the models from best to worst.

