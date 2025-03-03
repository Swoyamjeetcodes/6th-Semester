# theory - 

- introduction
- agents , Characteristics, agent function,
- PEAS
	- performance major, environment,  sensors, actuators,
- differ environment 
	- Fully Observable vs. Partially Observable
	- Deterministic vs. Stochastic
	- Episodic vs. Sequential
	- Static vs. Dynamic
	- Discrete vs. Continuous
	- Single Agent vs. Multiagent

- Agent types (with diagram)

- problem formulation (pg 111)
	- ex- 8 puzzel  
		- **Initial State**: A 3×3 grid with tiles placed in a random but valid configuration.
		- **Actions**: The blank tile can move left, right, up, or down (if within bounds).
		- **Transition Model**: Moving the blank tile swaps its position with the adjacent tile in the chosen direction.
		- **Goal Test**: The state matches the predefined goal configuration (e.g., tiles arranged in order from 1 to 8 with the blank at the bottom-right).
		- **Path Cost**: Each move has a uniform cost of 1 (total cost = number of moves).


# solve -

all algos => 
- Completeness: does it always find a solution if one exists?
- Time complexity: number of nodes generated
- Space complexity: maximum number of nodes in memory
- Optimality: does it always find a least-cost solution


## uninformed
- [bfs](https://www.youtube.com/watch?v=qul0f79gxGs)
- [ucs](https://www.youtube.com/watch?v=xkcR8-NEI1g)
- [dfs](https://www.youtube.com/watch?v=cq0cBynFFXI)
- [dls](https://www.youtube.com/watch?v=P7WQUBLKDmo)
- [ids](https://www.youtube.com/watch?v=BK8cEWKHCkY)
- [bidirec](https://www.youtube.com/watch?v=rEema9uQ02c)

## informed
- bestfs
	- [gbfs](https://www.youtube.com/watch?v=GVvN0ikNekw)
	- [A*](https://www.youtube.com/watch?v=iTG7NjQu0Qs)

## local search algo

- beam search algo

- [hill climbing (uses only h(n)!!)](https://www.youtube.com/watch?v=3SiWtAnUROs)
	- questions
		- [8 puzzel]()
		- n queen
		- [block world](https://www.youtube.com/watch?v=2SlO34_VsY4)
	- theory
		- Simulated Annealing (pg 353)
		- variants of HC (351)
		- [steepest vs basic](https://www.youtube.com/watch?v=Z1PjSvRC2vk)

- genetic algo
	- n queen

# irl problem

- [8 puzzel]
	- a*()
	- hill climbing
- [n queen]
	- gen ()
	- hill climbing

- [block world (hill climbing)](https://www.youtube.com/watch?v=2SlO34_VsY4)

- [monk and demon](https://youtu.be/yLEB-n4URu4)

## state space (theory)
- [water jug]()
- [vaccum cleaner](https://www.youtube.com/watch?v=ZBiHAUTYWVc)
