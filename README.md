Assignment 1 - Sorting & Removing Duplicates in a PS File
Manually create a file with 100 records, each 80 characters long, using ISPF (option 3.2).

The key is in positions 13-20, with 10 duplicate records.

Write a JCL script to:

Remove duplicate records.

Sort the remaining records in order based on the key.

Assignment 2 - Merging Two Files Based on Common Records
Create two separate files:

File1: 50 records, key at positions 13-20.

File2: 50 records, key at positions 21-28.

Write a COBOL program that:

Reads both files.

Creates a new file (File3) that contains only records that exist in both File1 and File2 (matching keys).

Assignment 3 - Sorting & Removing Duplicates Using REXX
Create a file with 120 records, each 100 characters long.

The key is in positions 25-32, with 15 duplicate records.

Write a REXX script to:

Remove duplicate records.

Sort the remaining records based on the key.

Assignment 4 - Sorting & Comparing Record Counts in JCL
Write a JCL script that:

Copies a PS or PO file into an output file and sorts it in descending order.

Compares the record count before and after sorting.

Keeps the output file only if the record count matches; otherwise, prints an error message.

Test it for both success and failure scenarios.

Assignment 5 - VSAM KSDS (Key-Sequenced Data Set) Handling in COBOL
Create a VSAM KSDS file with this structure:

Key: Customer ID (positions 1-8).

Data: Name (positions 9-40) and Address (positions 41-100).

Write a COBOL program to:

Insert 20 customer records.

Display records in order based on Customer ID.

Search for a customer ID entered by the user and display the record.

Assignment 6 - Managing a Generation Data Group (GDG)
Create a GDG base to store daily transaction logs. Each record:

Transaction ID: Positions 1-10.

Transaction Date: Positions 11-30.

Details: Positions 31-100.

Write a JCL script to:

Add a new generation with 10 sample transactions.

Use IDCAMS to list all generations.

Archive the last 3 generations into a PS file, then delete them from GDG.

Assignment 7 - Working with JCL and VSAM
Write a JCL script to:

Step 1: Create a VSAM KSDS file using IDCAMS.

Step 2: Load data from a PS file into this KSDS file using IDCAMS.

Step 3: Run LISTCAT to display details of the loaded KSDS dataset.

Assignment 8 - Working with GDG and JCL
Create a GDG base (define max generations and options like EMPTY/NOEMPTY, SCRATCH/NOSCRATCH).

Create new generations and add records:

First, write 4 records to GDG(+1).

Then, write 4 more to GDG(+2).

Repeat for GDG(+3) and GDG(+4).

Write a REXX script or SORT command to:

Merge GDG(+1) and GDG(+4) into one PS file (LRECL=80).

Merge GDG(+2) and GDG(+3) into another PS file (LRECL=80).

Example Output:
PS File 1 → Records from GDG(+1) and GDG(+4)
PS File 2 → Records from GDG(+2) and GDG(+3)