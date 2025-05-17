# LEETCODE-Arrays-75
Certainly! LeetCode 75: **Sort Colors** is a classic problem that asks you to sort an array containing only the values `0`, `1`, and `2` (representing red, white, and blue) **in-place** and **without using any built-in sort function**.

### 🔥 Optimal Approach: Dutch National Flag Algorithm

This uses **three pointers**: `low`, `mid`, and `high`.

### ✅ Java Code (No sort function used):

```java
public class SortColors {
    public void sortColors(int[] nums) {
        int low = 0, mid = 0, high = nums.length - 1;

        // Traverse the array
        while (mid <= high) {
            switch (nums[mid]) {
                case 0:
                    // Swap nums[low] and nums[mid], increment both
                    int temp0 = nums[low];
                    nums[low] = nums[mid];
                    nums[mid] = temp0;
                    low++;
                    mid++;
                    break;
                case 1:
                    // Move mid pointer
                    mid++;
                    break;
                case 2:
                    // Swap nums[mid] and nums[high], decrement high
                    int temp2 = nums[mid];
                    nums[mid] = nums[high];
                    nums[high] = temp2;
                    high--;
                    break;
            }
        }
    }

    // Optional: main method to test
    public static void main(String[] args) {
        SortColors sc = new SortColors();
        int[] colors = {2, 0, 2, 1, 1, 0};
        sc.sortColors(colors);
        
        // Print sorted array
        for (int color : colors) {
            System.out.print(color + " ");
        }
    }
}
```

### 🧠 How it works:

* `low`: Boundary for 0's
* `mid`: Current element
* `high`: Boundary for 2's
* Swapping happens only when `nums[mid]` is `0` or `2`
* Runs in **O(n)** time and **O(1)** space

Let me know if you'd like a version with comments in Hinglish or a step-by-step explanation!
