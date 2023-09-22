# Fokker-Planck-Equation-using-Physics-Informed-Neural-Networks-Deep-XDE

## Introduction
PINNs are an emerging 'type' of neural network, that is used mainly to solve physical problems that require computationally intensive solutions for PDEs and ODEs. 

## Traditional Methods and Their Limitations
Solving PDEs using Finite Difference Methods and Finite Element Methods means large matrix computations need to be done in order to reach a solution, providing a problem with a polynomial time complexity $O(n^3)$ for each matrix multiplication needed at each time step. This is a computationally intensive problem to solve, as it requires large computational power not available to many people, often needed GPUs to do the efficient computations. For larger systems, or highly non-linear PDEs, solutions computed with GPUs could still be too slow. Another limitation of these methods is that they require meshing, meaning the discretization of the set or region that the solution is found over. This further limits the resulting solution in terms of fineness and resolution.

## Neural Networks (NNs) as Universal Approximators
In come NNs, serving as universal approximators, with the capability of approximating essentially any function. This property allows for unprecedented flexibility in curve-fitting, with the constraints of specific functional forms a thing of the past. But how does this help solve a differential equation? In an experimental setting, the natural process being described by the PDE/ODE/Otherwise can be measured experimentally and sampled at different points or paths. This data can then be used to train NNs to generalize these results. 

## Challenges with NNs
However, only so much data could be produced by these experiments. This causes the training process to be difficult and rife with overfitting. More importantly, the NNs had no 'regard' for physical constraints, the predictions made by NNs were overfit so it did not obey basic conservation laws such as conservation of momentum, mass-energy, flow, etc. 

## Physics-informed Neural Networks (PINNs)
In a wonderful, in my opinion revolutionary, paper by Maziar Raissi, Paris Perdikaris, and George Em Karniadakis, they introduce the Physics-informed Neural Network (https://www.sciencedirect.com/science/article/pii/S0021999118307125). In an implementation that solves the prior problems with a simple technique of regularization based on common PDE constraints such as Dirichlet/VN/Robin Boundary conditions. It also suggests regularization by placing constraints in terms of conservation laws or rather fundamental laws for the system at hand (ex. The square-integrability of the wave function in case of the Schrodinger Wave Equation).

## DeepXDE for Physics-informed Machine Learning
In this example, I'm using a python package called DeepXDE (https://deepxde.readthedocs.io/en/latest/index.html) for physics-informed machine learning developed by George Em Karniadakis at Brown University and now maintained by Lu Lu at UPenn and other honorable members of the Lu Lu group (https://lu.seas.upenn.edu/). I highly recommend the reader go over their work, it is very interesting and I am for sure a great fan of their work.

## Project Focus
In this small project we will focus on solutions for the Fokker-Planck equation in its 2nd order form.

## To-Do List
Here are the next steps for this project:

1. **Further Training and Optimization**: Continue to train and optimize the network hyperparameters for improved performance.
2. **Solving the Generalized Fokker Planck Equation**: Attempt to solve the Generalized Fokker Planck Equation in its 4th order version.
3. **Comparison with Traditional Methods**: Compare the results obtained from the Physics-informed Neural Network with those from traditional Finite Difference Methods.

These steps will help in further enhancing the capabilities of the Physics-informed Neural Network and provide a comprehensive comparison with traditional methods.
