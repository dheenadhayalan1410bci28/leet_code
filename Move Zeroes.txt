void moveZeroes(int* nums, int numsSize) {
    int nonzero = 0; // Pointer for non-zero elements

    for (int i = 0; i < numsSize; i++) {
        if (nums[i] != 0) {
            // Swap non-zero element with the element at `nonzero`
            int temp = nums[i];
            nums[i] = nums[nonzero];
            nums[nonzero] = temp;
            nonzero++;
        }
    }
}
