
  
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


