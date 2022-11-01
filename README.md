# Leetcode
problem number 561 : Array Partition
->Take i and i++
  find the mininum element for both put in answer
  repeat for the another i and i++ while adding and return
  o(nlogn) 
  
  class Solution {
public:
    int arrayPairSum(vector<int>& nums) {
        int maxSum = 0;
        int i = 0;
        sort(nums.begin(),nums.end());
        while(i < nums.size())
        {
            maxSum = maxSum + min(nums[i], nums[i++]);
            i++;
        }
        return maxSum;
    }
};


