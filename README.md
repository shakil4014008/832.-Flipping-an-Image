# 832.-Flipping-an-Image
```C#
     public class Solution {
    public int[][] FlipAndInvertImage(int[][] A) {
        
        int n = A.GetUpperBound(0)+1;
        Console.Write(n+"-");
        for(int i=0; i<n; i++){
            for(int j=0; j<n/2; j++){
                
                int k = n-1-j;                
                int temp = A[i][j];
                A[i][j] = A[i][k]^1;
                A[i][k]=temp^1;
                
            }
            
            if(n%2 != 0){
                A[i][n/2] = A[i][n/2]^1;
            }
        } 
        
        return A;
    }
}
```

## Complexity Analysis
 
