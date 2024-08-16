# CS3.304 - Advanced Operating Systems

## Assignment 1 - Reversing Large Files

### Problem 1:
* This C++ project provides a solution to reverse the contents of a file and store the result in a new file within a directory named Assignment1.
* The program can either reverse the entire file or reverse specific portions of the file based on user input. The program is designed to handle large files efficiently, even when the file size exceeds available RAM.
* If the flag passed is 0 then complete input.txt file will be reversed
* If the flag passed is 1 then two aditional inputs i.e. start index and end index is passed. In this case file is reversed from beginning to the start index and from end index to end of the file.
* The reversed text file is stored into a new directory which is created in present working directory.

### Assumptions:
  * ##### Operating System:
      The program is intended to run on Unix-like systems (e.g., Linux, macOS) due to its use of POSIX system calls.
  * ##### Command Line Argument:
      * The First Argument is the input file length
      * The Second Argument is the flag
      * If the flag is 1, two additional input is required i.e. start_index and end_index
      * start_index and end_index should be a non negative integer

  ### How To Run: 
   * If we want to reverse the entire file
      ```bash
     
     $ ./a.out inputFilePath 0

     ```
     Example:
     ```bash
     $ ./a.out ./input.txt 0
     ```
     
   * If we want to reverse the file from start of file to start_index(excluded) and from end_index(excluded) to end of file
     ```bash
     $./a.out inputFilePath 1 start_index end_index
     ```
     Example:
     ```
      $./a.out ./input.txt 1 50 80
     ```



## Problem 2: 

  ### Overview:
  * This Program Check the permissions for the two files i.e. input.txt and output.txt created in the first problem and also of the directory created in the first problem.
  * Check whether the content in the new file created in Problem 1 are the reverse of the old file i.e. the input file provided.

  ### Assumptions:
   ##### Command Line Argument:
   * The First Argument is the <newFilePath>
   * The Second Argument is the <oldFilePath>
   * The third Argument is the <directoryPath>

 ### How to Run: 
  * To Run the program following the command format:
    ```bash
    $./a.out <newfile_path> <oldfile_path> <directory_path>
    ```
   Example: 
   ```bash
    $./a.out 1_input.txt input.txt Assignment1
   ```
