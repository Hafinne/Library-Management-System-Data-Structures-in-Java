Library Management System Using Custom Data Structures

This project is a console-based Library Management System implemented in Java.
It demonstrates the use of custom-built data structures instead of standard
Java collections to manage books, users, and transactions efficiently.
This project is a console-based Library Management System implemented in Java. 
The system allows users to manage a book catalog, search for books, handle 
borrow requests, and manage transactions using custom-built data structures.

Unlike standard Java collections, this project implements its own dynamic 
data structures to demonstrate understanding of their internal mechanics 
and algorithmic complexity.

------------------------------------------------------------------------
               DATA STRUCTURES & IMPLEMENTATION DETAILS
------------------------------------------------------------------------

1. DYNAMIC ARRAY (Catalog Management)
   - Used in: Storing all Book objects (Main Catalog).
   - Why: To handle an unknown number of books. It automatically resizes 
     (grows/shrinks) as books are added or removed, unlike fixed arrays.
   - Operations: Add, Remove, List All, Search by ID.

2. BINARY SEARCH TREE - BST (Search & Sort)
   - Used in: Searching books by Title and listing them alphabetically.
   - Why: BST provides efficient search operations (O(log n) on average) 
     and allows for easy alphabetical sorting via In-Order Traversal.
   - Operations: Search by Title, List Alphabetically.

3. QUEUE (Waiting List)
   - Used in: Managing borrow requests for books.
   - Why: Ensures a "First-Come, First-Served" (FIFO) policy for users 
     waiting for a book.
   - Operations: Enqueue (Request), Dequeue (Process Request).

4. STACK (Undo Feature)
   - Used in: Tracking Borrow and Return operations.
   - Why: Follows "Last-In, First-Out" (LIFO) logic, which is ideal for 
     reverting the most recent action (Undo).
   - Operations: Push (Save Action), Pop (Undo Last Action).

------------------------------------------------------------------------
                        FILE DESCRIPTIONS
------------------------------------------------------------------------
- Main.java         : Handles the user interface (console menu) and interaction.
- Library.java      : The manager class that integrates all data structures.
- DynamicArray.java : Custom implementation of a resizable array.
- BST.java          : Custom Binary Search Tree implementation.
- Queue.java        : Custom Queue implementation for requests.
- Stack.java        : Custom Stack implementation for undo operations.
- Book.java         : Represents a book entity (ID, Title, Author, Status).
- FileIO.java       : Helper class for reading/writing to txt files.
- books.txt         : Persistent storage for book data.
- users.txt         : Persistent storage for user logs and requests.

------------------------------------------------------------------------
                    HOW TO RUN THE PROJECT
------------------------------------------------------------------------
1. Ensure all .java files and .txt files are in the same directory.
2. Open a terminal/command prompt in the project folder.
3. Compile the code:
   javac Main.java
4. Run the application:
   java Main

------------------------------------------------------------------------
                    ADDITIONAL NOTES
------------------------------------------------------------------------
- Persistence: The system automatically loads data from 'books.txt' at 
  startup and saves changes after add/remove/borrow operations.
- IDs: Book IDs are auto-generated starting from 100 to prevent conflicts.
- Complexity: Worst-case time complexities are documented in the code 
  comments for each method.

========================================================================
