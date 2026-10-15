class Solution {
public:
    int search(vector<int>& nums, int target) {
        int left = 0;
        int right = nums.size() - 1;

        while (left <= right) {
            int mid = left + (right - left) / 2;

            if (nums[mid] == target) {
                return mid;
            }
            else if (nums[mid] < target) {
                left = mid + 1;
            }
            else {
                right = mid - 1;
            }
        }

        return -1;
    }
};

<img width="435" height="121" alt="image" src="https://github.com/user-attachments/assets/e71c0282-251d-48f3-b3ce-8cba104e015a" />

