class Solution {
public:
    int search(vector<int>& nums, int target) 
    {
        int n = nums.size();
        int low = 0, high = n - 1;
        while(low <= high)
        {
            int mid = (low + high) >> 1;
            if(nums[mid] > nums[n - 1])
                low = mid + 1;
            else
                high = mid - 1;
        }
        int index = low - 1;
        low = 0, high = index;
        while(low <= high)
        {
            int mid = (low + high) >> 1;
            if(nums[mid]==target)
                return mid;
            else if(nums[mid] > target)
                high = mid - 1;
            else
                low = mid + 1;
        }
        low = index + 1, high = n - 1;
        while(low <= high)
        {
            int mid = (low + high) >> 1;
            if(nums[mid]==target)
                return mid;
            else if(nums[mid] > target)
                high = mid - 1;
            else
                low = mid + 1;
        } 
        return -1;
    }
};
