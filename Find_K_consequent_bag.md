In Amazon's financial team an analyst is dealing with an infinite number of bags arranged in a line, each numbered from 1 to infinity. The task is to gather information about the amount of money in these bags, presented in the form of continuous segments. The objective is to select consecutive bags in such a way that the total amount of money in these bags is maximized.    
The continuous segments provided to represent the amount of money in each bag do not intersect. Additionally, any bag included within a segment contains some amount of money, while bags not included in any segment are considered to have zero money.    
Formally, given a 2D array segment of size n x 3, where n represents the number of available segments, and an integer k representing the number of consecutive bags you will take, and the 2D array segment represents the range of bags included in this segment [segment[0], segment[1]] and the amount of money inside the bags in the range segment[2].  
Find the k consecutive bags with the maximum total amount of money, since the answer can be large, return it modulo (109 + 7).      
Example    
k = 5    
n = 4    
int 3 (column size)     
segment = [ [1, 4, 2], [6, 6, 5], [7, 7, 7], [9, 10, 1] ]
The amount of money in each bag is:
Bag 1 2 3 4 5 6 7 8 9 10
Money 2 2 2 2 0 5 7 0 1 1
All other bags have zero money.  
Let's try different consecutive bags of size k:  
Bags Total Money  
[1 - 5] 2 + 2 + 2 + 2 + 0 = 8  
[2 - 6] 2 + 2 + 2 + 0 + 5 = 11  
[3 - 7] 2 + 2 + 0 + 5 + 7 = 16 
[4 - 8] 2 + 0 + 5 + 7 + 0 = 14  
[5 - 9] 0 + 5 + 7 + 0 + 1 = 13   
[6 - 10] 5 + 7 + 0 + 1 + 1 = 14  
The subsegment starting from the third bag and ending at the seventh bag has the maximum total amount of money, hence the answer is 16.    
Function Description 
Complete the function findMaximumMoney in the editor below.   
findMaximumMoney has the following parameters:  
int k: the  number of consecutive bags you will take.  
int segment[n][3]: A 2D array where n is the number of segments. Each segment contains the start index, end index, and money in the bags for that range.  
Returns 
int: the amount of money inside the k consecutive bags   with the maximum total amount of money modulo 109 + 7.      