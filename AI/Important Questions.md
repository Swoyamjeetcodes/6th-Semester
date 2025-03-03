># Important Questions 
> ## Q. Components of Problem Formulation for a Problem-Solving Agent
> ### 8-Puzzle (Sliding Tile) Problem
> The 8-puzzle consists of a 3×3 grid with 8 numbered tiles and 1 empty space, where tiles must be rearranged to reach the goal state.
> 
> - Initial State: A 3×3 grid with tiles placed in a random but valid configuration.
> - Actions: The blank tile can move left, right, up, or down (if within bounds).
> - Transition Model: Moving the blank tile swaps its position with the adjacent tile in the chosen direction.
> - Goal Test: The state matches the predefined goal configuration (e.g., tiles arranged in order from 1 to 8 with the blank at the bottom-right).
> - Path Cost: Each move has a uniform cost of 1 (total cost = number of moves).
> ### 8-Queens Problem
> The 8-queens problem requires placing 8 queens on an 8×8 chessboard such that no two queens attack each other.
> 
> - Initial State: An empty 8×8 chessboard.
> - Actions: Place a queen in any valid row of a column (typically one queen per column).
> - Transition Model: Adds a queen to the next column, ensuring no two queens attack each other.
> - Goal Test: All 8 queens are placed with no two attacking (no two in the same row, column, or diagonal).
> - Path Cost: Typically, no cost function is needed (only the solution matters), but constraint satisfaction approaches may count the number of conflicts.
>### **Problem Formulation for the Airline Travel Problem**  
>The **Airline Travel Problem** involves finding the best route from one city to another using available flights. This is a classic **graph-based search problem**, where cities are nodes and flights are edges.  
>
>#### **Components of Problem Formulation**  
>
>1. **Initial State**:  
>   - The departure city (starting location of the journey).  
>
>2. **Actions**:  
>   - The set of all available flights from the current city to other cities.  
>
>3. **Transition Model**:  
>   - If a flight is taken from city \( A \) to city \( B \), the new state is city \( B \).  
>
>4. **Goal Test**:  
>   - The destination city has been reached.  
>
>5. **Path Cost**:  
>   - Can be measured based on different criteria:  
>     - **Distance**: Total distance traveled (sum of flight distances).  
>     - **Time**: Total flight time, including layovers.  
>     - **Cost**: Total airfare price.  
>     - **Number of stops**: Minimizing layovers or flight transfers.  
> ## Q. From where do uninformed search strategies use the information?
> 
> Uninformed search strategies only use the following information provided in the problem formulation:
> - Initial State – The starting position of the search.
> - Actions – The set of possible moves or transformations from a given state.
> - Transition Model – The result of applying an action to a state.
> - Goal Test – A condition to check whether the current state is the goal.
> - Path Cost (if applicable) – The cost of reaching a state (for algorithms that consider cost, such as Uniform Cost Search).
> ## Q .Environment Types
> ### **1. Fully Observable vs. Partially Observable**
> - **Fully Observable**:  
>   If an agent’s sensors give it access to the complete state of the environment at each point in time, then the environment is effectively fully observable.  
>   **Examples**: Crossword puzzle, Chess with a clock, Image Analysis.  
> - **Partially Observable**:  
>   An environment might be partially observable because of noisy and inaccurate sensors or because parts of the state are missing from the sensor data.  
>   **Example**: A vacuum cleaner with only a local dirt sensor (no location detection) cannot tell whether other squares are clean or not.  
> ### **2. Deterministic vs. Stochastic**
> - **Deterministic**:  
>   If the next state of the environment can be completely determined by the current state and the actions executed by the agent, then the environment is deterministic.  
>   **Example**: Crossword Puzzle.  
> - **Stochastic**:  
>   If the next state cannot be fully determined by the current state and actions, the environment is stochastic.  
>   **Example**: Automated Taxi Driver.  
> - **Strategic**:  
>   Deterministic except for the actions of other agents.  
>   **Example**: Chess with a clock.
> ### **3. Episodic vs. Sequential**
> - **Episodic**:  
>   The agent's experience is divided into atomic "episodes." Each episode consists of the agent perceiving and then performing a single action. The choice of action in each episode depends only on the episode itself.  
>   **Example**: An agent spotting defective parts on an assembly line bases each decision on the current part, regardless of previous decisions.  
> - **Sequential**:  
>   In sequential environments, the current decision can affect all future decisions.  
>   **Examples**: Chess and Taxi driving are sequential—short-term actions can have long-term consequences.  
> ### **4. Static vs. Dynamic**
> - **Static**:  
>   The environment is unchanged while an agent is deliberating.  
> - **Semi-Dynamic**:  
>   The environment itself does not change with the passage of time, but the agent's performance score does.  
> - **Dynamic**:  
>   The environment changes while an agent is deliberating.  
> ### **5. Discrete vs. Continuous**
> - **Discrete**:  
>   A limited number of distinct, clearly defined percepts and actions.  
> - **Continuous**:  
>   The environment involves a continuous range of percepts and actions.  
> ### **6. Single Agent vs. Multiagent**
> - **Single Agent**:  
>   An agent operating by itself in an environment.  
> - **Multiagent**:  
>   More than one agent operates in the environment. It can be competitive or cooperative.
> ## Hill climbing is an optimization algorithm used to find the best possible solution by iteratively improving a candidate solution. Several variants exist to handle local optima and randomness in the search process. Here are three common variants:
> 
> ### 1. **Stochastic Hill Climbing**  
>    - Instead of always selecting the best neighbor, stochastic hill climbing selects a neighbor randomly and evaluates it.  
>    - If the new state is better than the current one, it moves to the new state; otherwise, it continues searching.  
>    - This introduces randomness, helping the algorithm escape local optima.  
> 
>    **Example**: Instead of choosing the highest elevation point among all neighbors, it randomly picks a few, evaluates them, and moves to a better one.
> ### 2. **First-Choice Hill Climbing**  
>    - A special case of stochastic hill climbing where the algorithm picks a random neighbor and immediately moves to it if it improves the solution.  
>    - It avoids evaluating all possible neighbors, making it useful for large search spaces.  
>    - It is faster than standard hill climbing because it does not check all neighbors before making a decision.
> 
>    **Example**: If you're trying to climb a mountain in fog, instead of scanning all possible paths, you randomly pick a nearby route and take a step if it goes uphill.
> ### 3. **Random-Restart Hill Climbing**  
>    - This method runs hill climbing multiple times from different random starting points.  
>    - Each run produces a local optimum, and the best among them is selected as the final solution.  
>    - Helps overcome the problem of getting stuck in a bad local optimum.
> **Example**: If you're searching for the highest peak in a hilly terrain, instead of starting from one location, you try from multiple places to increase your chances of finding the highest point.
> 
> ### Summary:
> | Variant                                            | Key Feature |
> |--------------------------------|------------|
> | **Stochastic Hill Climbing** | Picks a random neighbor instead of the best one |
> | **First-Choice Hill Climbing** | Picks the first improving neighbor found |
> | **Random-Restart Hill Climbing** | Runs hill climbing multiple times from random starts |
> 
> Each of these methods is useful in different scenarios depending on problem complexity and search space characteristics.