class Solution {
public:
    int singleNonDuplicate(vector<int>& nums) {
        int left = 0;
        int right = nums.size() - 1;

        while (left < right) {
            int mid = (left + right) / 2;

            if (mid % 2 == 1)
                mid--;

            if (nums[mid] == nums[mid + 1])
                left = mid + 2;
            else
                right = mid;
        }

        return nums[left];
    }
};

<img width="435" height="121" alt="image" src="https://github.com/user-attachments/assets/abf64c88-b1cb-4397-be24-c28e7211ef18" />

