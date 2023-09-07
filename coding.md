## Coding Questions
*Following are some of the important Coding Questions.*


### Question 1 : Two Sum
*Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.*

**Solution:**

```
//JS
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

```
//JS
var rotateString = function(s, goal) {
        if(s.length!=goal.length) {
                return false;
        }

        let temp = s+s;
        if (temp.includes(goal)) {
                return true;
        }
        
        return false;
};

```


----------------------------------------------

### Question 3 : Difference between Stack and Queue data structure

**Solution:**

**Stack:**

* A stack is a linear data structure that follows the Last-In-First-Out (LIFO) order, which means that the last element added is the first one to be removed.
* It supports two primary operations: push to add an element to the top of the stack and pop to remove the top element.
* Stacks are commonly used for tasks involving function call management, maintaining a history of actions for undo functionality, and evaluating expressions in postfix notation.
* Think of it like a stack of plates where you can only add or remove plates from the top.


**Queue:**

* A queue is another linear data structure that follows the First-In-First-Out (FIFO) order, meaning that the first element added is the first one to be removed.
* It supports two primary operations: enqueue to add an element to the back of the queue and dequeue to remove an element from the front.
* Queues are frequently used for tasks such as task scheduling in operating systems, managing print jobs in a printer, and handling incoming requests in a web server.
* Imagine it as a line of people waiting for a bus, where the person who arrived first is the first to board.


Following is the table showing the comparison: 


| Characteristic            | Stack                                    | Queue                                |
|---------------------------|------------------------------------------|--------------------------------------|
| Order of Access           | Last-In-First-Out (LIFO)                | First-In-First-Out (FIFO)            |
| Operations                | `push` (add to top), `pop` (remove top)  | `enqueue` (add to back), `dequeue` (remove front) |
| Use Cases                | Function call management, undo/redo, postfix expression evaluation | Task scheduling, request handling, breadth-first search |
| Examples                  | Browser history, undo functionality, recursive algorithms | Print job management, task scheduling in OS, web server requests |
| Data Structure Representation | Can be implemented with arrays or linked lists | Can be implemented with arrays or linked lists |
| Time Complexity (basic ops) | Typically `O(1)` for `push` and `pop` operations | Typically `O(1)` for `enqueue` and `dequeue` operations |


----------------------------------------------


### Question 4 : Return duplicate characters(in an array) from a given string

**Solution:**

```
//JS
function findDuplicates(str) {
  const charSet = new Set();
  const duplicates = [];

  for (const char of str) {   
    if (charSet.has(char)) {
      duplicates.push(char);
    } 

    else {
      charSet.add(char);
    }

  }

  return duplicates;
}

```

----------------------------------------------

### Question 5 : Check if a String contains only digits

**Solution:**

```
//JS
// '/\d/': In JavaScript regular expressions, / and / are delimiters used to define a regular expression pattern.
// '\d': This is a shorthand character class in regular expressions that matches any digit from 0 to 9.
// The test method checks if the string matches this regular expression and returns true if it does.


function containsOnlyDigits(str) {
  for (const char of str) {
    if (!/\d/.test(char)) {
      return false; 
    }
  }

  return true; 
}

```

----------------------------------------------

### Question 6 : Missing Number
*Given an array nums containing n distinct numbers in the range [0, n], return the only number in the range that is missing from the array.*

**Solution:**

```
//JS
var missingNumber = function(nums) {
    for(var i=0; i<=nums.length;i++){
        if(nums.includes(i)==false){
            return i
        }
    }   
       
};

```

----------------------------------------------

### Question 7 : Find the Duplicate Number
*Given an array of integers nums containing n + 1 integers where each integer is in the range [1, n] inclusive.*

*There is only one repeated number in nums, return this repeated number.*

*You must solve the problem without modifying the array nums and uses only constant extra space.*

**Solution:**

```
//JS
var findDuplicate = function(nums) {
    const numsSet = new Set();
    for (let i=0; i<=nums.length; i++) {
        if (numsSet.has(nums[i])) {
            return nums[i];
        }

        else {
            numsSet.add(nums[i]);
        }
    }   
};

```

----------------------------------------------

### Question 8 : Return the largest and the smallest integers in an unsorted integer array

**Solution:**

----------------------------------------------

### Question 9 : Contains Duplicate
*Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.*

**Solution:**

```
//JS
var containsDuplicate = function(nums) {
    const numSet = new Set();
    let check= false;

    for (let i=0; i<nums.length; i++) {
        if(numSet.has(nums[i])) {
            check = true;
        }

        else {
            numSet.add(nums[i])
        }
    }
    return check;
};

```

----------------------------------------------

### Question 10 : Reverse Words in a String
*Given an input string s, reverse the order of the words.*

*A word is defined as a sequence of non-space characters. The words in s will be separated by at least one space.*

*Return a string of the words in reverse order concatenated by a single space.*

*Note that s may contain leading or trailing spaces or multiple spaces between two words. The returned string should only have a single space separating the words. Do not include any extra spaces.*


**Solution:**

```
//JS
var reverseWords = function(s) {

    let temp = s.split(" ").reverse()
    return temp.filter(w=> w!== "").join(" ");
};

```

----------------------------------------------

### Question 11 : Design Linked List (Read JDK implementation)

**Solution:**

----------------------------------------------

### Question 12 : Middle of the Linked List

**Solution:**

----------------------------------------------

### Question 13 : Reverse Linked List
*Given the head of a singly linked list, reverse the list, and return the reversed list.*

**Solution:**


```
//C++
class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        ListNode* next = NULL;
        ListNode* prev = NULL; 
        
        while(head != NULL) {
            next = head->next;
            head->next = prev;
            prev = head;
            head = next;
        }
        head=prev;
        return head;
    }
};

```

----------------------------------------------
### Question 14 : Remove duplicate nodes in an unsorted linked list

**Solution:**

----------------------------------------------
