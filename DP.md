### 12.23 Wed
重新开刷。

### DP: base case + induction rule 数学归纳法  


Jump Game  
m[i]: represents 能否从开头跳到 i  
whether we can reach index i from the start.    
base case: m[0] 一定是 true  
回头看，都回头看谁。

A = [2, 3, 1, 1, 4]  
Result = true  
m[I] = if can jump from start to A[i]   
m[0] = true  
M[1] = (m[0] == true && if can jump from A[0] to A[1])   
M[2] = (m[0] == true && if can jump from A[0] to A[2] ||  
            m[1] == true && if can jump from A[1] to A[2])   
M[3] = (m[0] == true && if can jump from A[0] to A[3] ||  
            m[1] == true && if can jump from A[1] to A[3] ||  
            m[2] == true && if can jump from A[2] to A[3])   
….  

Base case: m[0] = true  
Induction rule: index j < current position I   
If m[j] == true && A[j] + j >= A[I] , we can jump to current position   





