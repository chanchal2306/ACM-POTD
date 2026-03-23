# Solution

class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        if (nums.size() == 0){
            return 0;
        }
        int og = 0;
        for( int dup = 1; dup<nums.size();dup++){
            if(nums[dup] != nums[dup-1]){
                nums[og+1] = nums[dup];
                og++;
            }
        }
        return og+1;
    }
};