
**Part 3** of [my book](https://ranja-sarkar.github.io/) consisting of two chapters briefly discusses methods of mathematical optimization.

<img width="523" alt="55" src="https://github.com/user-attachments/assets/abd24d03-d67b-4972-90a7-befa18fb83c5" />


# GRADIENT DESCENT 

Let's recapitulate [gradient descent](https://github.com/ranja-sarkar/GD/blob/main/README.md). 

It is an optimization algorithm utilized in regression models, neural networks to minimize a function called the loss function, also called cost function. It works by iteratively adjusting the model's parameters in the direction of the steepest descent of the function, aiming to find the minimum value point.

 <img width="554" alt="gd" src="https://github.com/user-attachments/assets/e234ca5a-4aae-4128-97fb-4765582e8900" />


#  Gradient & Hessian

Let us also recapitulate gradient and Hessian. 

Gradient is the vector of first order derivatives of a scalar field, which guides you with the direction in a landscape. 

<img width="820" height="312" alt="11" src="https://github.com/user-attachments/assets/b6451ca9-f744-4bfd-a31d-a64031848c39" />

Hessian is a matrix of second order partial derivatives of a scaler field. A Hessian not only guides, it tells if you're climbing, falling, or stuck in the landscape. Those points are inflexion points, extrema, and saddle points of the function. 

<img width="603" height="215" alt="22" src="https://github.com/user-attachments/assets/6ee5c768-3da2-4d37-b01b-3afebaa70e12" />

And Jacobian is a matrix of gradients of a vector field.

<img width="596" height="346" alt="33" src="https://github.com/user-attachments/assets/c725e397-b8a4-4a23-812f-e6244c079fe6" />


# Optimization problems

An objective function defines the goal of the optimization problem, specifying what needs to be maximized or minimized.
It's the function that  we try to optimize (either make as large or small as possible) based on the given constraints of the problem. 

Based on the types of objective function and constraint variables, [optimization problems](https://developers.google.com/optimization/introduction/python) can have 3 broad categories.   

<img width="356" alt="oo" src="https://github.com/user-attachments/assets/bae0bab4-7f72-4049-9ef0-2e9c1e3579d3" />

Optimization uses a rigorous mathematical model to determine the most efficient solution to a described problem. One must first identify an objective function (loss or cost), a quantitative measure examples of which are profit, cost, energy. The objective is subject to constraints such as resources, time. 

 1. **Linear Programming (LP)** 

    Example:

    Objective function: Goal is to maximize total profit, products A and B are sold at 25$ and 20$ respectively

    Constraints:
       1. Product A requires 20 resource units, product B 12 units
       2. Only 1800 resource units are available per day
       3. Both products require a production time of 1/15 hour
       4. A working day has a total of 8 hours.

    Mathematical Formulation:

       Objective function is maximizing total sales (x1 = #items of product A, x2 = #items of product B). Resource and time constraints are given by:

    <img width="419" height="193" alt="cf" src="https://github.com/user-attachments/assets/def837f1-fc0d-4198-93f3-937e17b3f143" />


 
 3. **Quadratic Programming (QP)** 
 
 4. **Non-Linear Programming** -> Objective function or (atleast one) constraint is non-linear


# Optimization with or without gradient

The categorization is strictly based on whether or not one can calculate or compute the gradient of objective function. The differentiability of the function makes us decide or choose the algorithm to use for the problem. This has been discussed in **chapter 10 of my book.** 

<img width="474" alt="5" src="https://github.com/user-attachments/assets/772ada5b-da96-40ab-a1c4-ac41130e3f7a" />

The space for searching global or local minimum solution wrt cost/objective function can be either continuous or discrete.  

<img width="437" alt="22" src="https://github.com/user-attachments/assets/f549e1c3-5f72-4e5a-b040-f9b5e1513427" />


An example of optimization problem with discrete variables in the objective function is the travelling salesman problem (TSP). It asks, "what’s the shortest possible route visiting every city once and returning to the start?" As the number of cities grows, brute-force solutions become computationally infeasible.

Read: https://diego.codes/post/som-tsp/

This repository contains an implementation of a Self-organizing Map that can be used to find sub-optimal solutions for TSP-> https://github.com/diego-vicente/som-tsp


For more on TSP: https://developers.google.com/optimization/routing/tsp

# Gradient-free optimizers

Well-known optimization algorithms for **continuous variables in the objective function** are simulated annealing, particle swarm method, genetic algorithm. 
These are the ones that do not use gradient to optimize the model.

1. **Simulated annealing**

   A Hill climbing algorithm is very basic optimization that explores a local search space. It starts at an initial point, which is often chosen randomly and continues to move to positions within its neighbourhood with a better solution. To execute it, we need to define the search space, step size of the algo, number of iterations, and an objective function. 

   <img width="429" alt="11" src="https://github.com/user-attachments/assets/79424819-04bb-4897-8861-4a720418e41d" />

It is a metaheuristic probabilistic technique to approximate optimization in a search (local) space of a physical process wherein the system energy is minimized.

Reference: https://simonblanke.github.io/gradient-free-optimizers-documentation/1.5/optimizers/simulated_annealing/

Simulated annealing chooses its next possible position similar to Hill climbing, but it accepts worse results with a probability that decreases with time. It simulates a temperature that decreases with each iteration, similar to a material cooling down. One of the algo parameters is annealing rate which is the rate at which the algorithmic temperature value decreases. 

[An annealing rate above 1 increases the temperature over time.]


2. **Genetic algorithm** (GA)

An evolutionary algorithm like GA is a stochastic, metaheuristic approach to solving problems that would take too long to exhaustively process using deterministic methods. 

GA is inspired by the process of natural selection that belongs to the larger class of evolutionary algorithms. Genetic algorithms are commonly used to generate high-quality solutions to optimization and search problems via biologically inspired operators such as selection, crossover, and mutation.

<img width="182" alt="33" src="https://github.com/user-attachments/assets/ca2d940c-b64c-4791-b056-0c2eb8834998" />

Reference: https://simonblanke.github.io/gradient-free-optimizers-documentation/1.5/optimizers/genetic_algorithm/main_page/

3. **Particle Swarm Optimization** (PSO)

PSO is a metaheuristic as it makes few or no assumptions about the problem being optimized and can search very large spaces of candidate solutions. It was first used to simulate social behavior. 

https://simonblanke.github.io/gradient-free-optimizers-documentation/1.5/optimizers/particle_swarm_optimization/

PSO does not use the gradient of the problem being optimized, which means it does not require that the optimization problem be differentiable as is required by classic optimization methods such as gradient descent and quasi-newton methods. The caveat is metaheuristics such as PSO do not guarantee an optimal solution is ever found.

# Summary of gradient-free optimization

Types of metaheuristic algorithms broadly:

<img width="572" alt="mh" src="https://github.com/user-attachments/assets/ae3cac4b-844a-48cf-8b48-3b2c035377a7" />

Local search -> The algorithm works by choosing new positions within a neighbourhood of the previous positions. It is recommended for convex optimization problems.

Global search -> The algorithm works by choosing new positions independently of the previous positions. It is recommended for non-convex optimization problems.
