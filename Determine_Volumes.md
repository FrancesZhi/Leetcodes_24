Determine the Volumes You Would Purchase Each Day  
👩‍🎓 NEW GRAD  
📚 AMAZON  

Amazon Books is a retail store that sells the newly launched novel "The Story of Amazon". The novel is divided into n volumes numbered from 1 to n and unfortunately, all the volumes are currently out of stock. The Amazon team announced that starting today, they will bring exactly one volume of "The Story of Amazon" in stock for each of the next n days. On the nth day, all volumes will be in stock. Being an impatient bookworm, each day you will purchase the maximum number of volumes you can such that:  

You have not purchased the volume before.  
You already own all prequels (prior volumes).  
Note: For the ith volume of the novel, all the volumes j such that j < i are its prequels. Determine the volumes you would purchase each day. You should return an array of n arrays where the ith array contains:  

the volume numbers sorted in increasing order if you purchased some volumes on the ith day  
the single element -1 if you did not purchase any book  
Example 1:  
Input:  volumes = [2, 1, 4, 3]  
Output: [[-1], [1, 2], [-1], [3, 4]]   
Explanation:  
      HEADS UP - the example output is AN EDUCATED GUESS. I will enhance it once find more reliable resources. The rest parts like problem statement, example input should at least give you an overall sense on what this question is asking. Be careful if you plan to solve this question. Dont let the educated guess output confuse you :) If you happen to know about the correct output, I am more than happy to make the modification. Many thanks in advance! You da best!!!  

      On day 1, volume 2 is available, but you cannot purchase it because volume 1 is not owned yet.  
      
      On day 2, volume 1 is available, and you purchase it along with volume 2 which was available from day 1.  
      
      On day 3, volume 4 is available, but you cannot purchase it because volumes 3 is not owned yet.  
      
      On day 4, volume 3 is available, and you purchase it along with volume 4 which was available from day 3.  
      
Constraints:
🥑🥑

Solution:

class Solution:
  def determinePurchases(self, volumes: List[int]) -> List[List[int]]:    