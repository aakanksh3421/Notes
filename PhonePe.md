##  Graphs 

### Course Order

[Course order](https://www.geeksforgeeks.org/find-whether-it-is-possible-to-finish-all-tasks-or-not-from-given-dependencies/) 

simple topo sort problem 
use **Kahn's alog** which is modified BFS 

Code :
`class Solution {`
  `public:`
    `vector<int> findOrder(int n, vector<vector<int>> prerequisites) {`

        `//this is basically topo sort , let us use Kahn's algo which is easier` 
        `// wat i had done prev was partially right , lets see abt this now` 
        `vector<int>inDegree(n,0);`
        `vector<vector<int>>adj(n);`
        
        `for(auto node : prerequisites){`
            `int dest = node[0];`
            `int src = node[1];`
            `adj[src].push_back(dest);`
            `inDegree[dest]++;`
        `}`
        
        `queue<int>q;`
        
        `for(int i = 0 ; i < n ; i++){`
            `if(inDegree[i] == 0) q.push(i);`
        `}`
        
        `vector<int>ans;`
        
        `while(!q.empty()){`
            `int a = q.front();`
            `q.pop();`
            `ans.push_back(a);`
            
            `for(auto lt : adj[a]){`
                `inDegree[lt]--;`
                `if(inDegree[lt] == 0 ) q.push(lt);`
            `}`
        `}`
        
        `if ((int)ans.size() == n) {`
            `return ans;`
        `} else {`
            `return {};`
        `}`
    `}`
`};`

## Frog Jump

2D - dp problem 

Code :

Recursive 
`class Solution {`
    `unordered_map<int,int>stone_map;`
    `int helper(int ind , int last ,  vector<int>&stones){`
    `if(ind == stones.size()-1) return true ;`

        `int arr[3] = {-1,0,1};`
        `for(int i = 0 ; i < 3 ; i++){`
            `int jump = last+arr[i];`
            `if(jump == 0 ) continue ;`

            `int next_pos = stones[ind] + jump;`
            `if(stone_map.find(next_pos) != stone_map.end()){`
                `int  next_ind = stone_map[next_pos];`
                 `if (helper(next_ind, jump, stones)) {`
                    `return true;`
                `}`
            `}`
        `}`
        `return false;`
    `}`
    `public:`
    `bool canCross(vector<int>& stones) {`
        `stone_map.clear();`
        `for (int i = 0; i < stones.size(); i++) {`
            `stone_map[stones[i]] = i;`
        `}`
        
        `return helper(0, 0, stones);`
    `}`
   `};`

memoised code 

