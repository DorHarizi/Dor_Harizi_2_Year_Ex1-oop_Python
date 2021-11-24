# Ex1

**Smart Elevator off-line algorithm with the following classes**

•	Ex1_Building: the building's main structure
•	Ex1_Calls: the calls main structure
•	Ex1_Elevator: the elevator's main structure
•	Ex1_allocate: allocating each call to the must suitable elevator
•	Ex1: loading and translating the json and csv file received by the user, sends the data to the allocate class, and outputs the calls allocation  

**Allocation algorithm**
Allocation algorithm is targeted to minimizing passenger wait by three main parameters taken in consideration:
•	the elevator's speed and the expected time the elevator will travel from floor a to floor b
•	the elevator's floor range – whether or not a certain elevator can reach the call's source and destination floor
•	the state of the elevator (UP, DOWN, LEVEL) 

**Algorithm features**

•	matching elevator is chosen based on the formula: state of the elevator + the expected time the elevator will travel from floor a to floor b
•	if pickup call happens in the same direction as a previous call it is assigned to the elevator already having this path
•	elevator picks up the passengers only in the same direction which minimizes their travel time in case elevator is going way too far in opposite direction
•	the Elevator's class will automatically create a matrix for each elevator. the matrix will represent the fastest time the elevator will travel from floor a to floor b, and has a main rule in the allocation system
