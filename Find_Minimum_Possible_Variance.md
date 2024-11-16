Find Minimum Possible Variance  
🤘 INTERN  
📚  
RELATED PROBLEMS
  
Within the Amazon Real Estate Analytics Toolset, an investor is evaluating a series of buildings of varying heights. The investor aims to find a group of buildings that adhere to two key conditions:  

The selected buildings must form a valid group.  
A group of buildings is considered valid if it meets the following criteria.  
It is a contiguous subsegment of the original array with a size of at least 2.  
The heights of the first and last buildings in this subsegment are the same.  
The group variance should be as minimal as possible.
The investor's goal is to find such a valid group of buildings with the minimal possible variance in height among the buildings in the group. The variance of a group is the difference between the size of the group and the occurrences of the first element height in the group, for example, the variance of the group (4, 2, 5, 4) is 4-2=2.  

Formally, given an array height of size n, the height of each building, find the minimum possible variance of a valid group of buildings, it is guaranteed that there is at least one valid group.  
 
An array a is a subsegment of an array b if a can be obtained from b by deletion of several (possibly, zero or all) elements from the beginning and several (possibly, zero or all) elements from the end. for example, [3, 1], and [4] is a subsegment of array [1, 3, 1, 4] while [1, 1], and [1, 4] is not.  

Example 1:  

Input:  height = [4, 2, 5, 4]  
Output: 2   
Explanation:  

      
      

      The group (4, 2, 5, 4) is a valid group because it is a contiguous subsegment of the original array, and the first and last building heights are the same. The variance of this group is the difference between the size of the group (4) and the occurrences of the first element height in the group (2), which is 4 - 2 = 2.
      


      
