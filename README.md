# Mainframe Assignments

## Overview
This document contains a set of assignments designed to enhance understanding of various mainframe concepts such as JCL, COBOL, REXX, VSAM, and GDG. The assignments focus on file handling, data processing, and job control language (JCL) operations.

## Assignments

### **Assignment 1 - Sorting & Removing Duplicates in a PS File**
- Create a Physical Sequential (PS) file with 100 records, each 80 bytes long.
- The primary key is in columns 13-20.
- 10 records are duplicates.
- Write a JCL SORT job to:
  - Remove duplicate records.
  - Sort the remaining records in ascending order based on the key.

### **Assignment 2 - Merging Two Files Based on Common Records**
- Create two PS files:
  - **File1:** 50 records with the key in columns 13-20.
  - **File2:** 50 records with the key in columns 21-28.
- Write a COBOL program to:
  - Read both files.
  - Create a new file (File3) containing only records that have matching keys in both files.

### **Assignment 3 - Sorting & Removing Duplicates Using REXX**
- Create a PS file with 120 records, each 100 bytes long.
- The primary key is in columns 25-32.
- 15 records are duplicates.
- Write a REXX script to:
  - Remove duplicate records.
  - Sort the remaining records based on the key.

### **Assignment 4 - Sorting & Comparing Record Counts in JCL**
- Write a JCL job to:
  - Copy a PS/PO file into an output file and sort it in descending order.
  - Compare the total record count before and after sorting.
  - Keep the output file only if the count matches, otherwise print an error message.
- Test scenarios where step b) succeeds and fails.

### **Assignment 5 - VSAM KSDS Handling in COBOL**
- Create a VSAM KSDS file with:
  - **Key:** Customer ID (columns 1-8).
  - **Data:** Customer Name (columns 9-40) and Address (columns 41-100).
- Write a COBOL program to:
  - Insert 20 customer records.
  - Display records in ascending order based on Customer ID.
  - Search for a specific Customer ID and display the corresponding record.

### **Assignment 6 - Managing a Generation Data Group (GDG)**
- Create a GDG base to store daily transaction logs with records:
  - **Transaction ID:** Columns 1-10.
  - **Transaction Date:** Columns 11-30.
  - **Transaction Details:** Columns 31-100.
- Write a JCL job to:
  - Add a new GDG generation with 10 sample transactions.
  - List all existing GDG generations using IDCAMS.
  - Archive the last 3 generations into a PS file and then delete them from GDG.

### **Assignment 7 - Working with JCL and VSAM**
- Write a JCL job to:
  - Step 1: Create a VSAM KSDS file using IDCAMS.
  - Step 2: Load a PS file into the KSDS file using IDCAMS.
  - Step 3: Run LISTCAT on the KSDS dataset and analyze the output.

### **Assignment 8 - Working with GDG and JCL**
- Create a GDG base with proper settings (LIMIT, EMPTY/NOEMPTY, SCRATCH/NOSCRATCH).
- Write records into multiple GDG generations:
  - GDG(+1): 4 records.
  - GDG(+2): 4 records.
  - GDG(+3): 4 records.
  - GDG(+4): 4 records.
- Write a REXX script or use SORT to:
  - Concatenate GDG(+1) and GDG(+4) into one PS file (LRECL=80, total records=4).
  - Concatenate GDG(+2) and GDG(+3) into another PS file (LRECL=80, total records=4).

## Technologies Used
- **JCL** (Job Control Language)
- **COBOL** (Common Business-Oriented Language)
- **REXX** (Restructured Extended Executor)
- **IDCAMS** (Integrated Data Cluster Access Method Services)
- **VSAM** (Virtual Storage Access Method)
- **GDG** (Generation Data Group)
- **SORT Utility**

## Prerequisites
- Basic understanding of mainframe operations.
- Familiarity with TSO/ISPF for file creation and editing.
- Knowledge of COBOL, JCL, and REXX scripting.

## How to Execute
1. Use **ISPF** to create and manage files.
2. Submit **JCL jobs** using **SDSF** to execute batch processing.
3. Run **COBOL programs** in a mainframe environment.
4. Execute **REXX scripts** using the TSO command prompt.
5. Use **IDCAMS** commands for VSAM and GDG management.

## Conclusion
These assignments will help you gain hands-on experience with mainframe file management, sorting, merging, and VSAM/GDG operations. Complete each assignment step by step and validate the output to ensure correctness.
