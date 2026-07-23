# Representation-of-a-Real-World-Problem-as-a-Markov-Decision-Process


## Aim

To model a real-world problem using a Markov Decision Process (MDP) for optimal decision-making in reinforcement learning.

Example:

> To model an e-commerce warehouse robot navigation problem as a Markov Decision Process (MDP) so that the robot can learn the optimal path to collect and deliver products while minimizing travel time and avoiding collisions.

---

## Problem Statement

### Problem Description

Problem

A robot collects products from shelves and delivers them to the packing station while avoiding obstacles and minimizing travel time.

MDP Component	Representation


Describe the real-world application that you selected.


---

## MDP Components

Agent	Warehouse Robot
Environment	Warehouse with shelves, obstacles, and packing station
States (S)	Robot's current location (e.g., Shelf A, Shelf B, Packing Station)
Actions (A)	Move Up, Down, Left, Right, Pick Item, Drop Item
Transition Probability (P)	If the robot moves right, it reaches the intended cell with probability 0.9 and slips to another cell with probability 0.1
Reward (R)	+100 for successful delivery, -20 for collision, -1 for each movement (to encourage shorter paths)
Discount Factor (γ)	0.9 (future rewards are important but slightly discounted)

A Markov Decision Process is represented as:

$$
MDP = (S, A, P, R, \gamma)
$$

Where:

| Symbol | Meaning |
|---|---|
| $S$ | Set of states |
| $A$ | Set of actions |
| $P$ | Transition probability function |
| $R$ | Reward function |
| $\gamma$ | Discount factor |

---

## State Space

Write your answer here.

The state space should list all possible situations in which the agent can exist.

Example format:

```text
S = {
    State 1,
    State 2,
    State 3,
    ...
}
```



---

## Sample State

Write your answer here.

A sample state is one specific example from the state space.



---

## Action Space

Write your answer here.

The action space should list all possible actions available to the agent.

Example format:

```text
A = {
    Action 1,
    Action 2,
    Action 3,
    ...
}
```


---

## Sample Action

Write your answer here.

A sample action is one action selected from the action space.



---

## Transition Probability

Write your answer here.

The transition probability explains how the environment moves from one state to another after an action is taken.

General form:

$$
P(s' \mid s,a)
$$

This means:

> Probability of reaching next state $s'$ after taking action $a$ in current state $s$.


---

## Reward Function

Write your answer here.

The reward function defines the feedback received by the agent after taking an action.

General form:

$$
R(s,a,s')
$$



---

## Graphical Representation

Write your answer here.

Draw the MDP graph.

The graph should include:

1. States as nodes.
2. Actions as arrows.
3. Rewards on transitions.
4. Transition probabilities if applicable.


---

## Python Representation

Write your code here.

Use Python dictionaries to represent the MDP.


```python
# MDP Representation using Python
# print("Name:       ")
# print("Register Number:     ")

```
---
## Output

Write your Python output here.


---

## Result

Write your result here.



---

