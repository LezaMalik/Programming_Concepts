## Coding Questions
*Following are some of the important Coding Questions.*


### Question 1 : Two Sum
*Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.*

**Solution:**

```
var twoSum = function(nums, target) {
    
    for (let i=0; i<nums.length-1; i++) {
        for (let j=i+1; j<nums.length; j++) {
            if (nums[i] + nums[j] == target) { 
                return [i, j];
            }       
        }
    }  
};
```
----------------------------------------------

