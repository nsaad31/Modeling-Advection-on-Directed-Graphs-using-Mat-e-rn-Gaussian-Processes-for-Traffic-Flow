# Modeling-Advection-on-Directed-Graphs-using-Mat-e-rn-Gaussian-Processes-for-Traffic-Flow

We utilize our DGAMGP model for traffic modeling on synthetic and real-world directed traffic graphs.  

We test on synthetic generated data and real-world directed traffic data from the California Performance Measurement System with the road network graph from the Open Street Map \cite{osm2017}. For the synthetic data, we generate data that models the situation of traffic on a road. 

The data $\mathcal{D} = (x_i, y_i)_{i=1}^N$ denotes the traffic flow speed in miles per hour $y_i$ at location $x_i$. We test our model's predictive ability to predict the velocities of cars on a road at different positions.  We use hold-out cross validation to split the data points generated into training (70\% of the data) and testing data (30\% of the data).  We extend the code in https://github.com/spbu-math-cs/Graph-Gaussian-Processes to compute the singular value decomposition of $L_{adv}$ to train our DGAMGP model on a directed graph
