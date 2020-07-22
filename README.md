# Monte Carlo Q Learning on Simple Self Defined Environment

## Environment

it is like below:
**(a simple grid based env)**

```
 E  .  .  .
 .  .  . .
 S  .  .  .
 .  .  .  E
```
Where, 
* E --> terminal / end point
* S --> start point --> initially at (2, 0)

### How it works

The agent starts from **S** and learns the optimal policy to reach the end point. the reward are set as below:
```
(0, 0) --> 0
(3, 3) --> 0
```
The overall grid with initial defined rewards look like below:
```
---------------------------
 0.00|-1.00|-1.00|-1.00|
---------------------------
-1.00|-1.00|-1.00|-1.00|
---------------------------
-1.00|-1.00|-1.00|-1.00|
---------------------------
-1.00|-1.00|-1.00| 0.00|
```
Possible actions that the agent can take are:
* U (up)
* D (down)
* L (left)
* R (right)

### Final Q table after 10000 Episodes
```
Q table: 
----------------------------------------------
| State  | U      | D      | L      | R      |
----------------------------------------------
| (0, 0) |   0.00 |   0.00 |   0.00 |   0.00 |
| (0, 1) |  -1.18 |  -2.67 |   0.00 |  -2.56 |
| (0, 2) |  -2.83 |  -4.45 |  -1.52 |  -4.76 |
| (0, 3) |  -4.03 |  -7.43 |  -3.41 |  -6.30 |
| (1, 0) |   0.00 |  -2.71 |  -1.46 |  -2.65 |
| (1, 1) |  -1.46 |  -3.76 |  -1.45 |  -3.74 |
| (1, 2) |  -2.70 |  -4.87 |  -3.69 |  -4.93 |
| (1, 3) |  -4.31 |  -6.26 |  -9.94 |  -8.55 |
| (2, 0) |  -1.45 |  -3.63 |  -2.64 |  -3.62 |
| (2, 1) |  -2.77 |  -4.08 |  -2.69 |  -4.50 |
| (2, 2) |  -3.81 |  -4.37 |  -4.89 |  -5.44 |
| (2, 3) |  -7.41 |   0.00 |  -5.34 |  -6.04 |
| (3, 0) |  -2.65 |  -3.76 |  -3.69 |  -4.39 |
| (3, 1) |  -4.35 |  -4.93 |  -3.50 |  -3.99 |
| (3, 2) | -10.00 |  -9.99 |  -5.64 |   0.00 |
| (3, 3) |   0.00 |   0.00 |   0.00 |   0.00 |
----------------------------------------------
```
The agent chooses the maximum value for each state to find the optimal policy. 
## Reference
* I learned it from the repository described [here](https://github.com/ravasconcelos/monte_carlo) and [here](https://colab.research.google.com/drive/1yJwMgv3XSZ6mLcZ1W7JAxLRZVBjHOXea?usp=sharing)
