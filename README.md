# diagonal-matrix-sum-s-logic
This repository contains my solution to the Leet Code problem "Diagonal Sum of a Matrix," showcasing efficient matrix traversal and summation logic.
below is the code I wrote for this problem:
class Solution {
public:
    int diagonalSum(vector<vector<int>>& mat) {
        int sum;
        int sum1 = 0;
        int sum2 = 0;
        int final;
        int sum3;
        for(int i = 0; i < mat.size(); i++){
            int j = i;
            if(mat.size() % 2 != 0){
                sum3 = mat[(mat.size() - 1)/2][(mat.size() - 1)/2];
            }
            else{
                sum3 = 0;
            }
            sum1 += mat[i][j];
            sum2 += mat[i][mat.size()- 1 - i];      
        }
        sum = sum1 + sum2;
        final = sum - sum3;
        return final;
    }
};
