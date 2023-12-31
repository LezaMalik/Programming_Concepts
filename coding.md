## Coding Questions
*Following are some of the important questions related to general coding.*




### Question 1 : Two Sum
*Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.*

*You may assume that each input would have exactly one solution, and you may not use the same element twice.*

*You can return the answer in any order.*

**Solution:**

```
//lang: JS

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
//lang: JS

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
//lang: JS

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
//lang: JS

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
//lang: JS

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
//lang: JS

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

```
//lang: JS

function findMinMax(arr) {
    if (arr.length === 0) {
        return null; 
    }

    let min = arr[0];
    let max = arr[0];

    for (let i = 1; i < arr.length; i++) {
        if (arr[i] < min) {
            min = arr[i];
        }
        if (arr[i] > max) {
            max = arr[i];
        }
    }

    return { min, max };
}


```

----------------------------------------------

### Question 9 : Contains Duplicate
*Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.*

**Solution:**

```
//lang: JS

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
//lang: JS

var reverseWords = function(s) {

    let temp = s.split(" ").reverse()
    return temp.filter(w=> w!== "").join(" ");
};

```

----------------------------------------------

### Question 11 : Design Linked List (Read JDK implementation)

**Solution:**

```
//lang: C++

class Node {
public:
    int data;
    Node* next;
  
    // Default constructor
    Node()
    {
        data = 0;
        next = NULL;
    }
  
    // Parameterised Constructor
    Node(int data)
    {
        this->data = data;
        this->next = NULL;
    }
};
  
// Linked list class to implement a linked list.
class Linkedlist {
    Node* head;
  
public:
    // Default constructor
    Linkedlist() { head = NULL; }
  
    // Function to insert a node at the end of the linked list.
    void insertNode(int);
  
    // Function to print the linked list.
    void printList();
  
  
};


// Function to insert a new node.
void Linkedlist::insertNode(int data)
{
    // Create the new Node.
    Node* newNode = new Node(data);
  
    // Assign to head
    if (head == NULL) {
        head = newNode;
        return;
    }
  
    // Traverse till end of list
    Node* temp = head;
    while (temp->next != NULL) {
  
        // Update temp
        temp = temp->next;
    }
  
    // Insert at the last.
    temp->next = newNode;
}
  
// Function to print the nodes of the linked list.
void linkedlist::printList()
{
    Node* temp = head;
  
    // Check for empty list.
    if (head == NULL) {
        cout << "List empty" << endl;
        return;
    }
  
    // Traverse the list.
    while (temp != NULL) {
        cout << temp->data << " ";
        temp = temp->next;
    }
}

```

----------------------------------------------

### Question 12 : Middle of the Linked List

**Solution:**

```
//lang: C++

ListNode* findMiddle(ListNode* head) {
    ListNode* slow = head;
    ListNode* fast = head;

    while (fast != NULL && fast->next != NULL) {

      slow = slow->next;         // Movs One Step
      fast = fast->next->next;  // Moves Two Steps
    }

    return slow;
}

```

----------------------------------------------

### Question 13 : Reverse Linked List

*Given the head of a singly linked list, reverse the list, and return the reversed list.*

**Solution:**


```
//lang: C++

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

### Question 14 : Remove duplicate nodes in an unsorted linked list.

**Solution:**

```
//C++

void removeDuplicates(struct Node* start)
{
    struct Node *temp1, *temp2, *duplicateNode;
    temp1 = start;
 
    // Pick elements one by one 
    while (temp1 != NULL && temp1->next != NULL) {
        temp2 = temp1;
 
        // Compare the picked element with rest of the elements 
        while (temp2->next != NULL) {

            /* If duplicate then delete it */
            if (temp1->data == temp2->next->data) {
                duplicateNode = temp2->next;
                temp2->next = temp2->next->next;
                delete (duplicateNode);
            }
            else 
                temp2 = temp2->next;
        }
        temp1 = temp1->next;
    }
}

```

----------------------------------------------

### Question 15 : Count Primes

*Given an integer n, return the number of prime numbers that are strictly less than n.*

**Solution:**

```
//lang: JS

var countPrimes = function (n) {
  
    let hashArray = new Array(n).fill(true);   // initialize all elements to 'true'

    // Set the first two elements (0 and 1) to 'false' since they are not prime
    hashArray[0] = false, hashArray[1] = false;

    // Iterate from 2 to the square root of 'n'
    for (let i = 2; i * i < n; i++) {
        // For each 'i', iterate through multiples of 'i' starting from 'i^2'
        for (let j = i * i; j < n; j += i) {
            // Mark the multiples of i as 'false' in the 'hashArray'
            hashArray[j] = false;
        }
    }

    return hashArray.filter((num) => num == true).length;
};

```

*Explanation:*

* Create a List: Begin by creating a list of consecutive integers from 2 to n: [2, 3, 4, .., n].

* Start with the First Prime: The first prime number is 2. Mark it as a prime and start with it.

* Eliminate Multiples: For each prime number p, iterate through the list and eliminate all multiples of p greater than p. To do this, mark numbers like 2 * p, 3 * p, 4 * p, etc., as non-prime.

* Find the Next Unmarked Number: Find the smallest unmarked number in the list that is greater than the current prime number p. This will be the next prime number.

* Repeat: Repeat steps 3 and 4 until the square of the current prime number is greater than n. At this point, all remaining unmarked numbers in the list are prime.

* Result: The remaining unmarked numbers in the list are all prime numbers less than or equal to n.


----------------------------------------------

### Question 16 : Valid Palindrome


*A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.*

*Given a string s, return true if it is a palindrome, or false otherwise.*

**Solution:**

```
//lang: JS

var isPalindrome = function(s) {
  s = s.toLowerCase().replace(/[^a-z0-9]/gi,'');
  for (let i = 0, j = s.length - 1; i < j; i++, j--) {
    if (s[i]!==s[j]) return false;
  }
  return true;
}
    

```

----------------------------------------------

### Question 17 : 

*Given *

**Solution:**



----------------------------------------------