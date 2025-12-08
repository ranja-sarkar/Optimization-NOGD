

# LP example

 **Objective function**:
 
 1. Goal is to maximize total profit
 2. Products A and B are sold at 25$ and 20$ respectively

    
 **Constraints**:
 
 1. Product A requires 20 resource units, product B 12 units
 2. Only 1800 resource units are available per day
 3. Both products require a production time of 1/15 hour
 4. A working day has a total of 8 hours.

**Mathematical Formulation:**

Objective function maximizes total sales. 

<img width="168" alt="13" src="https://github.com/user-attachments/assets/d225fbc3-289d-4983-8f5a-124f4b2d5e0e" />

Resource and time constraints are given by:

<img width="353" alt="14" src="https://github.com/user-attachments/assets/9913411c-25df-48f5-90e0-0c1e5aa5d3f1" />


x1 = #items of product A, x2 = #items of product B


<img width="389" alt="15" src="https://github.com/user-attachments/assets/0bff54c7-e77b-4961-95e3-143b3753a6d4" />

Optimal x1 and x2 are 45 and 75 respectively.

Blog on LP in python: https://mlabonne.github.io/blog/posts/2022-03-02-Linear_Programming.html


# QP example

Portfolio optimization: https://www.cvxpy.org/examples/basic/quadratic_program.html

Convex optimization: https://www.cvxpy.org/

An excerpt from my book (chapter 4) where I briefly touched upon convex functions and their optimization.

<img width="402" alt="16" src="https://github.com/user-attachments/assets/34ae602c-6954-4c89-92d3-a737ab992bc2" />

When we talk about convex and concave functions, we think of the **Hessian**. The Hessian matrix has two important utilities:
- to know whether a function is concave or convex

<img width="562" alt="22" src="https://github.com/user-attachments/assets/c2114793-4dd7-43df-b504-9019046439ad" />
  
- to determine whether a critical point is a local minimum, a local maximum, or a saddle point [If the gradient of a function is zero at some point, that is f(x)=0, then function f has a critical point at x]


<img width="563" alt="11" src="https://github.com/user-attachments/assets/d2ddebdb-e5a9-49e8-b5cd-45ea0065f09d" />


<img width="199" alt="pp" src="https://github.com/user-attachments/assets/85c5f867-00f3-4750-bc4e-7c63b06d87a9" />


In general, QP in python: https://scaron.info/blog/quadratic-programming-in-python.html

# NLP example


<img width="425" alt="12" src="https://github.com/user-attachments/assets/3226387d-f786-4df7-a43a-b965595c6d87" />


Solving nonlinear optimization problems with multiple python libraries: 

https://github.com/marcelcases/nonlinear-optimization

NLP with python: https://paulminogue.com/posts/a0d8c837-a40d-4b17-9d30-e0bd36a6befc

