// It is a preblem to modify array in-place, which means we can't use another auxiliary data structure.
// The answer is to use two-pointers.
// One of the pointer go through the array faster, and another go through the array slower.

// Two pointer (one approach)
class Solution {
    public int removeDuplicates(int[] nums) {
        int i = 0;
        for (int j = 1; j < nums.length; j++) {
            if (nums[i] != nums[j]) {
                i++;
                nums[i] = nums[j];
            }   
        }
        return i + 1;  
    }
}
