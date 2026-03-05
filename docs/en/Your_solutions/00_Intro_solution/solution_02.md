# Solving a System of Linear Equations

## Necessary Definitions & Formulas

**System of Linear Equations:** A set of two or more linear equations that share the same set of variables. To "solve" the system means to find the exact values of the variables that make all the equations true at the same time. Geometrically (for two variables), this represents the point where two lines intersect on a graph.

**Substitution Method:**
A highly effective algebraic method for solving systems of equations. The formula/steps are as follows:
1. **Isolate:** Solve one of the equations for one variable in terms of the other (e.g., isolate $x$ to get $x = f(y)$).
2. **Substitute:** Plug this expression into the *other* equation. This creates an equation with only one variable.
3. **Solve:** Solve the new single-variable equation.
4. **Back-Substitute:** Plug the found numerical value back into the isolated expression from Step 1 to find the remaining variable.

---

## Problem Statement

Find the values of $x$ and $y$ that satisfy both equations:

$$
2x + 3y = 12
$$

and

$$
x - y = 1
$$

---

## Step-by-Step Solution

### Step 1: Isolate a variable
It is usually easiest to isolate a variable that has a coefficient of 1 or -1. Let's look at the second equation and isolate $x$.

We start with:

$$
x - y = 1
$$

Add $y$ to both sides of the equation to isolate $x$:

$$
x = y + 1
$$

### Step 2: Substitute the expression into the other equation
Now, take the expression for $x$ that we just found and substitute it into the *first* equation. 

The first equation is:

$$
2x + 3y = 12
$$

Replacing $x$ with $(y + 1)$:

$$
2(y + 1) + 3y = 12
$$

### Step 3: Solve for the remaining variable ($y$)
First, distribute the $2$ into the parentheses:

$$
2y + 2 + 3y = 12
$$

Combine the like terms ($2y$ and $3y$):

$$
5y + 2 = 12
$$

Subtract $2$ from both sides to isolate the $y$ term:

$$
5y = 10
$$

Divide by $5$:

$$
y = 2
$$

### Step 4: Back-substitute to find the first variable ($x$)
Now that we have the numerical value for $y$, substitute it back into our isolated expression from Step 1 to quickly find $x$.

$$
x = y + 1
$$

Substitute $y = 2$:

$$
x = 2 + 1
$$

$$
x = 3
$$

### Step 5: Verification
It is always good practice to check your answers by plugging both values back into the original equations.

Check Equation 1 ($2x + 3y = 12$):

$$
2(3) + 3(2) = 6 + 6 = 12
$$

Check Equation 2 ($x - y = 1$):

$$
3 - 2 = 1
$$

Both statements are true, confirming our solution is correct!

---

## Final Answer

The values that satisfy the system of equations are:

$$
x = 3, \quad y = 2
$$
