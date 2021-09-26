# Modeling-Advection-on-Directed-Graphs-using-Mat-e-rn-Gaussian-Processes-for-Traffic-Flow

We utilize our DGAMGP model for traffic modeling on synthetic and real-world directed traffic graphs.  

We test on synthetic generated data and real-world directed traffic data from the California Performance Measurement System with the road network graph from the Open Street Map \cite{osm2017}. For the synthetic data, we generate data that models the situation of traffic on a road. 

The data <img src="https://render.githubusercontent.com/render/math?math=\mathcal{D} = (x_i, y_i)_{i=1}^N"> denotes the traffic flow speed in miles per hour <img src="https://render.githubusercontent.com/render/math?math=y_i"> at location <img src="https://render.githubusercontent.com/render/math?math=x_i">. We test our model's predictive ability to predict the velocities of cars on a road at different positions.  We use hold-out cross validation to split the data points generated into training (70\% of the data) and testing data (30\% of the data).  We extend the code in https://github.com/spbu-math-cs/Graph-Gaussian-Processes to compute the singular value decomposition of <img src="https://render.githubusercontent.com/render/math?math=L_{adv}"> to train our DGAMGP model on a directed graph

## Examples

Notebook using the advection operator solve a regression problem on PEMS data [[2]](https://github.com/VeritasYin/STGCN_IJCAI-18/blob/master/data_loader/PeMS-M.zip) is
> jupyter notebook  examples/Regression_new_operators_cleaned-advec-svd-finite-difference-upwind.ipynb 

The data in `examples/data` is third-party, and only provided in the repo to facilitate running the examples.


## Citation
```
@inproceedings{borovitskiy2021matern,
      title={Matern Gaussian Processes on Graphs}, 
      author={Viacheslav Borovitskiy and Iskander Azangulov and Alexander Terenin and Peter Mostowsky and Marc Peter Deisenroth and Nicolas Durrande},
      booktitle={International Conference on Artificial Intelligence and Statistics},
      year={2021},
      organization={PMLR}
}
