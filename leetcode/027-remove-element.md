# 027-Remove element


* https://leetcode.com/problems/remove-element/description/

* Approach 1:
```java
// One approach
// It also can be solved by two-pointers
class Solution {
    public int removeElement(int[] nums, int val) {
        int i = 0;
        for (int j = 0; j < nums.length; j++) {
            if (nums[j] != val) {
                nums[i] = nums[j];
                i++;
            }
        }
        return i;
    }
}
```

* Approach 2:
```java
// Another approach using two-pointers

// The element need to be deleted could be rare.
// Try another way of two-pointers.
class Solution {
    public int removeElement(int[] nums, int val) {
        int current = 0;
        int length = nums.length;
        while (current < length) {
            if (nums[current] == val) {
                // No need to update the current pointer.
                // The current pointer need to check again. The only thing we need to do is minus the length by 1.
                nums[current] = nums[length - 1];
                length--;
            } else {
                current++;
            }
        }
        return length;
    }
}
```