## Basic Programming Concepts
*Following are some of the important programming concepts.*




### 1. What's ASCII?
ASCII (American Standard Code for Information Interchange) is a character encoding standard that assigns a unique 7-bit binary number to each alphanumeric character, punctuation mark, and control character used in English text. It was widely used in early computer systems and communication protocols.

Characters in ASCII encoding include upper and lowercase letters A through Z, numerals 0 through 9 and basic punctuation symbols. It also uses some non-printing control characters that were originally intended for use with teletype printing terminals.

ASCII characters may be represented in the following ways:

* as pairs of hexadecimal digits -- base-16 numbers, represented as 0 through 9 and A through F for the decimal values of 10-15;
* as three-digit octal (base 8) numbers;
* as decimal numbers from 0 to 127; or
* as 7-bit or 8-bit binary

Following is the ASCII Table: 

![ASCII picture](./data/ASCII.JPG)

----------------------------------------------

### 2. What's Unicode?
Unicode is a universal character encoding standard that encompasses characters from all languages and scripts used worldwide. Unlike ASCII, which is limited to 128 characters, Unicode assigns a unique code point (a numeric value) to each character, allowing representation of a vast range of symbols, alphabets, and characters.

Unicode provides a unique number for every character including punctuation marks, mathematical symbols, technical symbols, arrows, and characters making up non-Latin alphabets such as Thai, Chinese, or Arabic script. Since its inception, Unicode has been adopted by all modern software providers, allowing the transportation of data through devices, applications, and platforms without corruption. It is now used in all major operating systems, browsers, search engines, laptops, smartphones, and across the internet.

Following is the UNICODE Table: 

![unicode picture](./data/unicode.png)

----------------------------------------------

### 3. What's utf-8?
UTF-8 (Unicode Transformation Format - 8-bit) is a variable-width character encoding that's widely used on the internet and in computing. It can represent any Unicode character using one to four bytes. UTF-8 is backward-compatible with ASCII, meaning ASCII characters are represented as a single byte, while extended characters use multiple bytes.

Spatial efficiency is a key advantage of UTF-8 encoding. If instead every Unicode character was represented by four bytes, a text file written in English would be four times the size of the same file encoded with UTF-8.

Another benefit of UTF-8 encoding is its backward compatibility with ASCII. The first 128 characters in the Unicode library match those in the ASCII library, and UTF-8 translates these 128 Unicode characters into the same binary strings as ASCII. As a result, UTF-8 can take a text file formatted by ASCII and convert it to human-readable text without issue.



![utf picture](./data/utf.PNG)

----------------------------------------------

### 4. How is text data stored on disk?
Text data is stored on disk as binary data using a character encoding like UTF-8. Each character is translated into its corresponding binary representation according to the chosen encoding. When reading the data, the encoding is used to interpret the binary values and convert them back into characters.

----------------------------------------------

### 5. Explain Modern Hardware Architecture
Modern hardware architecture involves a CPU with multiple cores, fast RAM, various types of storage (SSD, HDD), and peripherals connected through buses. The CPU executes instructions, cores allow parallel processing, RAM holds data for active tasks, and storage retains persistent data. Buses enable communication between components.

----------------------------------------------

### 6. What's the max RAM in 32-bit and 64 bit? and why?
A 32-bit system can theoretically address up to 4 GB of RAM because memory addresses are 32 bits wide. A 64-bit system can address much more memory (terabytes or more) due to its larger memory address space, which enhances performance and supports memory-intensive applications.

----------------------------------------------

### 7. How many bits in a byte
A byte consists of 8 bits.

----------------------------------------------

### 8. Write decimal 0-7 in binary
0: 000
1: 001
2: 010
3: 011
4: 100
5: 101
6: 110
7: 111

----------------------------------------------

### 9. Convert decimal to binary

----------------------------------------------

### 10. What is hex?
Hexadecimal (hex) is a base-16 numbering system using digits 0-9 and letters A-F. It's used to represent binary data more compactly and is often used in low-level programming and memory addressing.

----------------------------------------------

### 11. What is JSON?
JSON (JavaScript Object Notation) is a lightweight data interchange format. It uses human-readable text to represent data objects consisting of attribute-value pairs. It's commonly used for APIs and configuration files.

----------------------------------------------

### 12. What is XML? What is root, element, attributes, and text?
XML is a markup language for structuring data hierarchically. 
The root is the top-level element, containing child elements. 
Elements are tagged data items with optional attributes (metadata). 
Text represents content within elements.

----------------------------------------------

### 13. What is CSV? What is header? how does escape work?
CSV is a text-based format for tabular data. It uses commas to separate values in columns. The first row often contains headers that label the columns. Special characters within values are escaped using techniques like enclosing in double quotes.

----------------------------------------------

### 14. What is Parquet?
Parquet is a columnar storage file format designed for analytics. It stores data in columns, enabling better compression and query performance. Parquet is commonly used in big data processing frameworks like Apache Spark.

----------------------------------------------

### 15. What is GIT? 
Git is a distributed version control system for tracking changes in source code. It allows multiple developers to collaborate on a project, manage versions, and maintain a history of changes.

----------------------------------------------
### 16. Explain GIT flow with diagram (master/dev/feature/release/)
----------------------------------------------

### 17. What is PR (pull request)?
A Pull Request (PR) is a request to merge code changes from one branch (often a feature branch) into another branch (such as dev or master). It facilitates code review and collaboration among team members.

----------------------------------------------

### 18. Git pull/push/add/commit/checkout/branch/clone

* *git pull:* Fetches changes from a remote repository and integrates them into the current branch.
  
* *git push:* Uploads local changes to a remote repository.
  
* *git add:* Stages changes for commit.
  
* *git commit:* Records staged changes in the repository.
  
* *git checkout:* Switches between branches or commits.
  
* *git branch:* Lists, creates, or deletes branches.
  
* *git clone:* Creates a local copy of a remote repository.


----------------------------------------------
