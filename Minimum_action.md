
There's a computer system owned by an Amazon user. This system is equipped with n CPU cores, each with a specific temperature denoted by temperature[I].  
The user, let's call them the Optimizer, is keen on enhancing the performance of their machine by regulating the core temperatures. In a single operation, the Optimizer can choose one of the following techniques:
Select a position i (0 ≤ i < n) and decrease the temperature of the CPU cores 0, 1, … i by 1.  
Select a position i (0 ≤ i < n) and decrease the temperature of the CPU cores i, i+1, ... n -1 by  
Increase the temperature of all cores by 1.
Formally, given an array temperature of size n, the initial temperature of each core, find the minimum number of actions required for the Optimizer, to make the temperature of each core equal to 0.  


Example    
n = 3  
temperature = [2, 4, 4]     
One of the optimal ways to make the temperature of all cores 0 is as follows:
Select index 1 and use the ability of type 2. The new temperatures will be [2, 3, 3].
Select index 2 and use the ability of type 1. The new temperatures will be [1, 2, 2].
Select index 1 and use the ability of type 2. The new temperatures will be [1, 1, 1].
Select index 2 and use the ability of type 1. The new temperatures will be [0, 0, 0].
It can be shown that it is not possible to make the temperature of each core equal to 0 in less than 4 actions, hence, the answer is 4.
Function Description  
Complete the function regulateTemperatures in the editor below.     
regulateTemperatures has the following parameter:      
int temperature[n]:  initial temperature of each core     
Returns      
long:  the minimum number of actions required to make the temperature of each core equal to 0.  