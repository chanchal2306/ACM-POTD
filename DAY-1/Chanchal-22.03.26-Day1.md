# Solution

class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int length = nums.size();
        vector<int> ans ;
        for (int i = 0 ; i <= length ; i++){
           // int first = nums[i]; 
           for ( int j = i+1 ; j< length; j++) {
                //int second = nums[j];
               if (nums[i] + nums[j] == target) {
                    ans.push_back(i);
                    ans.push_back(j);
                    break;
               }
           }
        }
        
        return ans;
    }
};