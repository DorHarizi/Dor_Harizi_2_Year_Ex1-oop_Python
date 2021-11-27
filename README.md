## Assignment 1 - Object Oriented Programming :office: :elevator:
**Dor Harizi**  
**Yuval Shabt**
---
The project is about utilizing a building which is composed from a number of elevators and their parameters in the most efficient way for less waiting time of each person.  
In the project we will receive 2 files, a building file in json format and calls in csv format, calls are composed from few components the main ones are source floor and destination floor. In the algorithm we will try to determine what is the most efficient waiting time solution for the given problem.

Reference to the UML: [ click here](#Smart-Elevator-UML)  
Reference to how to use: [ click here](#How-to-use)

---
## Elevator Algorithm:

According to a research shown in the sources, it can be seen that zoning has proved to have the best average wait time for each people.
As a result we decided that our offline algorithm will be deviding the calls into zones and assigning the calls according to the speed of the elevator.

## Algorithm features

•	Matching elevator is chosen based on the formula: state of the elevator + the expected time the elevator will travel from floor a to floor b
•	If pickup call happens in the same direction as a previous call it is assigned to the elevator already having this path
•	Elevator picks up the passengers only in the same direction which minimizes their travel time in case elevator is going way too far in opposite direction
•	The Elevator's class will automatically create a matrix for each elevator. the matrix will represent the fastest time the elevator will travel from floor a to floor   b, and has a main rule in the allocation system

---

## Here are our results for the avarage waiting time:
   - **The B1...B5 represents each of the buildings we tested.** 
   - **The Calls_a...Calls_d  represents each of the calls scenario we tried.** 
   - The buildings B1, and B2 can be tested only on calls_a because this is the only scenario with calls that are in the floor range of these buildings. (-2,10)  

|           | **B1** | **B2** | **B3** | **B4** | **B5** |
|-----------|--------|--------|--------|--------|--------|
|**Calls_a**|	112.9	 | 68.69  | 54.44  | 66     |	26.7   |
|**Calls_b**|		     |        | 762.2  | 785.6  |	469.2  |
|**Calls_c**|		     |        | 775.8  | 831.1  |	505    |
|**Calls_d**|		     |        | 775.8  | 831.1  |	505    |  

 *Values were rounded to 1 digit after the decimal point.*    
 
---
##Smart Elevator UML:

<p align="center">
    <img width="800" height="900" src="https://github.com/DorHarizi/Dor_Harizi_2_Year_Ex1-oop_Python/blob/main/uml.png">
   </p>
   
---


## How to use:
Clone the repository and cd(enter) the folder.
```
git clone https://github.com/DorHarizi/Dor_Harizi_2_Year_Ex1-oop_Python.git & cd Dor_Harizi_2_Year_Ex1-oop_Python
```
To insert your own building and call files you can use this option
```
python Ex1.py <building_json_file_name> <calls_csv_file_name> <output_file_name>
```
To use existing building and call files use this command
```
python Ex1.py <output_file_name>
```
## Testing jar
In order to test the results run the following
```
java -jar Ex1_checker_V1.2_obf.jar <IDs, building, calls, log_out>
```  
* `IDs` : at least 1 ID seperated by "," maximum 3.  
* `building` : the json file representing the building  
* `calls` : the csv file representing the calls  
* `log_out` : the output file name   

------
