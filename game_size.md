Get Minimum Pen Drive Size  
👩‍🎓 NEW GRAD  
📚 AMAZON  
Within the Amazon Gaming Distribution System, a logistics coordinator is faced with the task of efficiently distributing n games among k different children. Each game is characterized by its size, denoted by gameSize[i] for 1 ≤ i ≤ n.
  
To facilitate the distribution process, the coordinator opts to utilize pen drives, ordering k pen drives with identical storage capacity. Each pen drive can receive a maximum of 2 games, and every child must receive at least one game, also no game should be left unassigned.

Considering the impracticality of transferring large game files over the internet, the strategy involves determining the minimum storage capacity required for the pen drives. A pen drive can only store games if the sum of their sizes does not exceed the pen drive's storage capacity.

What is the minimum storage capacity of pen drives that you must order to be able to give these games to the children?

Function Description

Complete the function getMinSize in the editor.

getMinSize has the following parameters:

int gameSize[n]: the size of each game
int k: the number of children amongst whom the games are to be distributed
Returns

int: an integer variable denoting the minimum capacity of pen drives required to distribute the games amongst the children

Example 1:

Input:  gameSize = [9, 2, 4, 6], k = 3
Output: 9 
Explanation:

      
We note that we will need pen drives of the size of at least 9 units, to store the first game.

This also turns out to be the minimum size of pen drives that should be ordered to give the games to these children.

We can use the first pen drive to store the game of size 9, the 2nd one to store the second and third games, and the 3rd pen drive to store the fourth game.

Hence, the minimum capacity of pen drives required is 9 units.
     
      
Constraints:
1 ≤ k ≤ n ≤ 2 * 10^5
1 ≤ gameSize[i] ≤ 10^9
n ≤ 2*k


# binary search
<pre>
def check(gameSize,k,size_mid):
    games_size = len(gameSize)
    one_pen_drives = 2k - games_size
    two_pen_drives = games_size - k 
    # one+2* two == games_size
    # one  = games_size -(2games_size-2k) = 2k - games_size
    gameSize.sort()
    gameSize.reverse()
    if gameSize[0] > x :
        return False 
    gameSize = gameSize[2k - games_size:]
    for i in range(len(gameSize)):
        if gameSize[i] +gameSize[len(gameSize)-1-i] >x :
            return False
    return True
    
def getMinSize(self, gameSize: List[int], k: int) -> int:

    left = 0
    right = int(1e9)
    result = right 

    while left <= right:
        mid = (left +right) //2
        if check(k,mid,):

        right = mid -1

        else:
            left = mid+1
    return result
 </pre>  