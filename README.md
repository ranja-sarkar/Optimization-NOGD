# Optimization

**Part 3 of my book consisting of two chapters** briefly discusses methods of mathematical optimization.⬇️

<img width="523" alt="55" src="https://github.com/user-attachments/assets/abd24d03-d67b-4972-90a7-befa18fb83c5" />


Buy the book from Amazon: https://a.co/d/h3cRD25

----

Recap of GRADIENT DESCENT - optimization method used in machine learning to minimize a function, often the loss function. It works by iteratively adjusting the model's parameters in the direction of the steepest descent of the function, aiming to find the minimum value.

 <img width="554" alt="gd" src="https://github.com/user-attachments/assets/e234ca5a-4aae-4128-97fb-4765582e8900" />

 ----

# Optimization problems


An objective function defines the goal of the optimization problem, specifying what needs to be maximized or minimized.
It's the function that  we try to optimize (either make as large or as small as possible) based on the given constraints of the problem. 

Based on the types of objective function and constraint variables, optimization problems can have 3 broad categories.   

<img width="356" alt="oo" src="https://github.com/user-attachments/assets/bae0bab4-7f72-4049-9ef0-2e9c1e3579d3" />

**Read the optimization markdown file to know more about them.** 

Solving various optimization problems using Google ORTools (python): https://developers.google.com/optimization/introduction/python

-----

# Optimization methods

The categorization is strictly based on whether or not one can calculate or compute the gradient of objective function. 

<img width="474" alt="5" src="https://github.com/user-attachments/assets/772ada5b-da96-40ab-a1c4-ac41130e3f7a" />

The space for searching global or local minimum solution wrt cost/objective function can be either continuous or discrete.  

<img width="437" alt="22" src="https://github.com/user-attachments/assets/f549e1c3-5f72-4e5a-b040-f9b5e1513427" />


An example of optimization problem with discrete variables in the objective function is the travelling salesman problem (TSP). It asks, "what’s the shortest possible route visiting every city once and returning to the start?" As the number of cities grows, brute-force solutions become computationally infeasible.

Read: https://diego.codes/post/som-tsp/

This repository contains an implementation of a Self-organizing Map that can be used to find sub-optimal solutions for TSP-> https://github.com/diego-vicente/som-tsp


For more on TSP: https://developers.google.com/optimization/routing/tsp

-------------

Well-known **optimization algorithms** for **continuous variables** in the objective function are simulated annealing, particle swarm method, genetic algorithm. 
These are the ones that do not use gradient to optimize.

1. **Simulated annealing**

   <img width="429" alt="11" src="https://github.com/user-attachments/assets/79424819-04bb-4897-8861-4a720418e41d" />

It is a metaheuristic probabilistic technique to approximate optimization in a search (local) space of a physical process wherein the system energy is minimized.

Reference: https://simonblanke.github.io/gradient-free-optimizers-documentation/1.5/optimizers/simulated_annealing/

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
