### Q1. What is the recommended strategy for dealing with strong interference in a communication channel?
* Treat the interference as noise.
* Ignore the interference.
* Decode the interference.
* Increase the transmission power.

### Q2. The Han Kobayashi idea is a strategy for:
* Channel capacity in Rayleigh fading.
* Decoding semantic states.
* Rate splitting in an interference channel.
* Calculating ergodic capacity.
* No correct answers.

### Q3. What is the primary characteristic of an "Interference Channel"?
* A single sender communicates with multiple receivers.
* Multiple senders try to communicate with their own receivers, but their signals interfere.
* There is no noise, only signal distortion.
* The channel capacity is always zero.

### Q4. Consider the Interference Ordered Semantic Channel Matrix $P_s(K \to l)$. How would this matrix fundamentally differ from a simple point-to-point semantic channel matrix if the "semantics of all other users" are such that they are highly correlated with the intended user's semantics?
* The matrix $P_s(K \to l)$ would become an identity matrix, indicating perfect communication.
* The off-diagonal probabilities in $P_s(K \to l)$ might increase, as the receiver's interpretation could be influenced by the semantic context of other users.
* The matrix would be impossible to define, as the conditioning would make it non-ergodic.
* The matrix would be the same as the point-to-point matrix, as the conditioning on other users is irrelevant.

### Q5. A binary broadcast channel has two receivers: Receiver 1 (BSC with crossover probability 0.1) and Receiver 2 (BSC with crossover probability 0.25). Find the capacity of both links and identify the stronger user.
* 0.531 bits/use; 0.189 bits/use; Receiver 2 is the strong user, Receiver 1 is the weak (degraded) user
* 0.531 bits/use; 0.189 bits/use; Receiver 1 is the strong user, Receiver 2 is the weak (degraded) user
* 0.691 bits/use; 0.189 bits/use; Receiver 1 is the strong user, Receiver 2 is the weak (degraded) user
* 0.531 bits/use; 0.485 bits/use; Receiver 1 is the strong user, Receiver 2 is the weak (degraded) user

### Q6. Gaussian Broadcast Channel
**Given:**
* Total power $P = 10$
* Noise powers: $N_1 = 1$, $N_2 = 4$
* Power split $\alpha = 0.6$

**Find $R_1$ and $R_2$:**
* 0.531 bits/use; 0.189 bits/use
* 0.531 bits/use; 0.159 bits/use
* 1.40 bits/use; 0.24 bits/use
* 1.40 bits/use; 0.485 bits/use

### Q7. Consider a two-user wireless communication system where the received signal is given by:
$$Y = H_1 X_1 + H_2 X_2 + Z$$

**In this model:**
* $X_1$ and $X_2$ are the transmitted symbols from User 1 and User 2, respectively.
* $H_1$ and $H_2$ are the real-valued fading coefficients for the two users.
* $Z$ is the additive white Gaussian noise (AWGN) with mean zero.

**Consider two different channel conditions with fixed transmitted powers $X_1 = X_2 = 1$ and fixed noise $Z = 0.5$:**
* **Condition I:** $H_1 = 10$, $H_2 = 10$
* **Condition II:** $H_1 = 10$, $H_2 = 0.1$

Calculate the total received signal $Y$ for both conditions. Identify which condition is interference-limited and which is noise-limited. Justify your answer by comparing the relative strengths of the desired signal, interference, and noise.
* 20.5; 10.6; Condition I is Interference-Limited; Condition II is Noise-Limited
* 10.5; 10.6; Condition I is Interference-Limited; Condition II is Noise-Limited
* 20.5; 10.9; Condition I is Interference-Limited; Condition II is Noise-Limited
* 20.5; 10.6; Condition I is Noise-Limited; Condition II is Interference-Limited

### Q9. A food delivery platform uses semantic states:
* **Delivery Person 1:** {Order Picked Up, En Route, Nearby, Delivered}
* **Delivery Person 2:** {Restaurant Delay, Traffic Jam, Wrong Address, Completed}
* **Customer 1:** Wants to know "When will my food arrive?"

**Part A: Baseline Matrix**
Design a 4×4 conditional semantic channel matrix for Delivery Person 1 $\to$ Customer 1 when Delivery Person 2 sends "Completed" (low interference). All diagonal elements should be $\ge 0.90$.

**Part B: Interference Matrix**
Design the conditional matrix when Delivery Person 2 sends "Restaurant Delay" (high interference). Show how this semantically similar message creates confusion between "Order Picked Up" and "En Route" states specifically.

**Part C: Task-Specific Aggregation**
Customer 1's true task is only to know if delivery time is: {Imminent (Nearby/Delivered), Not Imminent (Picked Up/En Route)}. Collapse your 4×4 matrix from Part B into a 4×2 task-oriented matrix. Explain the aggregation logic.

**Part D: Alignment Strategy**
Propose how Delivery Person 2 could encode "Restaurant Delay" messages to minimize semantic interference for Customer 1's task.
