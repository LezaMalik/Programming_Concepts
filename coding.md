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

### Question 2 : Rotate String 
*Given two strings s and goal, return true if and only if s can become goal after some number of shifts on s.*

*A shift on s consists of moving the leftmost character of s to the rightmost position.*

*For example, if s = "abcde", then it will be "bcdea" after one shift.*


**Solution:**



----------------------------------------------

### Question 3 : Difference between Stack and Queue data structure
----------------------------------------------
### Question 4 : Return duplicate characters(in an array) from a given string
----------------------------------------------
### Question 5 : Check if a String contains only digits
----------------------------------------------
### Question 6 :Missing Number
----------------------------------------------
### Question 7 : Find the Duplicate Number
----------------------------------------------
### Question 8 : Return the largest and the smallest integers in an unsorted integer array
----------------------------------------------
### Question 9 : Contains Duplicate
----------------------------------------------
### Question 10 : Reverse Words in a String
----------------------------------------------
### Question 11 : Design Linked List (Read JDK implementation)
----------------------------------------------
### Question 12 : Middle of the Linked List
----------------------------------------------
### Question 13 : Reverse Linked List
----------------------------------------------
### Question 14 : Remove duplicate nodes in an unsorted linked list
----------------------------------------------