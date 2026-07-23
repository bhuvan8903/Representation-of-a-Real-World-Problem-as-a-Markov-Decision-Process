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

Describe the real-world application that you selected.

The selected real-world application is an e-commerce warehouse robot. The robot collects products from shelves and delivers them to the packing station while avoiding obstacles and minimizing travel time. At each step, it observes its current location, chooses an action, and receives rewards based on its performance. This problem can be modeled as a Markov Decision Process (MDP) because it involves sequential decision-making to maximize long-term rewards.

---

## MDP Components


A Markov Decision Process is represented as:

$$
MDP = (S, A, P, R, \gamma)
$$

Where:

| Symbol | Meaning |
|---|---| 
| $S$ | The set of possible states of the environment|
| $A$ | The set of actions the agent can perform. |
| $P$ | The probability of moving from one state to another after taking an action. |
| $R$ | The immediate reward received after taking an action. |
| $\gamma$ | A value between 0 and 1 that determines the importance of future rewards. |

---

## State Space
```
S = {
    Start,
    At Shelf A,
    At Shelf B,
    Carrying Item,
    At Packing Station,
    Delivery Completed,
    Collision
}
```


The state space should list all possible situations in which the agent can exist.

---

## Sample State

```
Sample State:
At Shelf A
```

A sample state is one specific example from the state space.



---

## Action Space

A = {
    Move Up,
    Move Down,
    Move Left,
    Move Right,
    Pick Item,
    Drop Item
}
The action space should list all possible actions available to the agent.

---

## Sample Action

```
Sample Action:
Pick Item
```
Description:
The robot picks up the required product from Shelf A before moving toward the packing station.

A sample action is one action selected from the action space.

---

## Transition Probability
The transition probability defines the likelihood of moving from one state to another after taking an action.
$$
P(s′∣s,a)
$$
where:

s = Current state
a = Action taken
s′= Next state

Example:
```
P(At Shelf B | At Shelf A, Move Right) = 0.9
P(Collision | At Shelf A, Move Right) = 0.1
```
This means the robot reaches Shelf B with a probability of 0.9 after moving right from Shelf A, while there is a 0.1 probability of colliding with an obstacle or ending up in an unintended state.

---

## Reward Function

Reward Function

The reward function provides feedback to the robot after performing an action and moving to the next state.
$$
R(s,a,s′)
$$
where:

s = Current state
a = Action taken
s′= Next state

Example:
```
R(At Shelf A, Pick Item, Carrying Item) = +10
R(Carrying Item, Drop Item, Delivery Completed) = +100
R(At Shelf A, Move Right, Collision) = -20
R(At Shelf A, Move Right, At Shelf B) = -1
```
This means:

+10 for successfully picking up an item.
+100 for successfully delivering the item.
-20 for colliding with an obstacle.
-1 for each movement to encourage the robot to choose the shortest path.

---

## Graphical Representation

Write your answer here.

Draw the MDP graph.

                 Move Right
Start ------------------------> At Shelf A
                                  |
                                  | Pick Item (+10)
                                  v
                           Carrying Item
                                  |
                                  | Move Right (-1)
                                  | P = 0.9
                                  v
                        At Packing Station
                                  |
                                  | Drop Item (+100)
                                  v
                       Delivery Completed

        Move Right
At Shelf A ---------------------> Collision
             P = 0.1              Reward = -20

Explanation:

States (nodes): Start, At Shelf A, Carrying Item, At Packing Station, Delivery Completed, Collision.
Actions (arrows): Move Right, Pick Item, Drop Item.
Rewards: +10 for picking the item, +100 for successful delivery, -1 for movement, -20 for collision.
Transition Probabilities: 0.9 for successful movement and 0.1 for collision.


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

