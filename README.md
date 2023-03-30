# Leetcode - 二分查找

**正常实现**  

```cpp
int binarySearch(vector<int> nums, int key) {
    int l = 0, r = nums.length - 1;
    while (l <= r) {
        int p = l + (r - l) / 2;
        if (nums[p] == key) {
            return p;
        } else if (nums[p] > key) {
            r = p - 1;
        } else {
            l = p + 1;
        }
    }
    return -1;
}
```
