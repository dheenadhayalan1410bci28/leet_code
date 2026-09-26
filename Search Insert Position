int searchInsert(int* nums, int numsSize, int target) {
        for (int i = 0 ; i < numsSize ; i++){
            if(nums[i]==target){
                return i;
            }
        }
        int q=numsSize-1;
        while(q>=0){
            if(target==0 && nums[0]>0){
                return 0;

            }
            if(nums[q]<target){
                return q+1;
            }
            else if(nums[0]>target){
                return 0;
            }
            q--;
            
        }
        
        if (numsSize == 1 && target>nums[0]){
            return 1;
        }
        else if (numsSize == 1 && target<nums[0]){
            return 0;
        }
        return -1;
}
