# Optimization

**Part 3 of my book consisting of two chapters** briefly discusses methods of mathematical optimization. ⬇️

<img width="523" alt="55" src="https://github.com/user-attachments/assets/abd24d03-d67b-4972-90a7-befa18fb83c5" />


Buy the book from Amazon: https://a.co/d/h3cRD25

-----

# Categories of optimization algorithms

This is strictly based on whether or not one can calculate or compute the gradient of objective function. 

<img width="474" alt="5" src="https://github.com/user-attachments/assets/772ada5b-da96-40ab-a1c4-ac41130e3f7a" />

The space for searching global or local minimum solution wrt cost/objective function can be continuous or discrete.  

<img width="437" alt="22" src="https://github.com/user-attachments/assets/f549e1c3-5f72-4e5a-b040-f9b5e1513427" />


Well-known **optimization algorithms** for **continuous variables** in the objective function are simulated annealing, particle swarm method, genetic algorithm. 
These are also the ones that do not use gradient to optimize.

1. **Simulated annealing**

   <img width="429" alt="11" src="https://github.com/user-attachments/assets/79424819-04bb-4897-8861-4a720418e41d" />

It is a metaheuristic probabilistic technique to approximate global optimization in a large search space of a physical process wherein the system energy is minimized.

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


