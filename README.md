# OS-Kernel-Simulator

OVERVIEW:
- This program implements a simple OS kernel scheduling simulator using the C programming language. It implements 3 scheduling algorithms (FCFS, External Priorities, and Round Robin), as well as a memory management algorithm.

This project  Folder is split into 4 sub folders + README.md file:
1. `README.md`: this is read file you are currently reading.
2. FCFS Folder:
	1. `FCFS.c`: this file contains the C code that we wrote that implements a first come first serve algorithm.
	2. `FCFS.exe`: this is the executable file for the project.
	3. `Test files test_case_1.csv -> test_case_10.csv`: there are 10 test .csv files that can be used to test the algorithm
	4. `Batch files test1.bat -> test10.bat`: there are 10 .bat files that will be used to run the test_case_1.csv -> test_case_10.csv test files.
3.  ExternalPriorities Folder:
	1. `ExternalPriorities.c`: this file contains the C code that we wrote that implements the external priorties algorithm.
	2. `ExternalPriorities.exe`: this is the executable file for the project.
	3. `Test files test_case_1.csv -> test_case_10.csv`: there are 10 test .csv files that can be used to test the algorithm
	4. `Batch files test1.bat -> test10.bat`: there are 10 .bat files that will be used to run the test_case_1.csv -> test_case_10.csv test files.
4.  RoundRobin Folder:
	1. `RoundRobin.c`: this file contains the C code that we wrote that implements the round robin algorithm.
	2. `RoundRobin.exe`: this is the executable file for the project.
	3. `Test files test_case_1.csv -> test_case_11.csv`: there are 11 test .csv files that can be used to test the algorithm
	4. `Batch files test1.bat -> test11.bat`: there are 11 .bat files that will be used to run the test_case_1.csv -> test_case_11.csv test files.
5.  MemoryManagement Folder (Implemented using First Fit Algorithm):
	1. `MemoryManagement.c`: this file contains the C code that we wrote that implements the MemoryManagement algorithm for the first partition given to us in the assignment document.
	2. `MemoryManagement.exe`: this is the executable file for the project.
	3. `Test files test_case_1_P1.csv -> test_case_10_P1.csv`: there are 10 test .csv files that can be used to test the algorithm with this partition.
	4. `Batch files test1.bat -> test10.bat`: there are 10 .bat files that will be used to run the test_case_1.csv -> test_case_10.csv test files.

HOW TO RUN:
- Each algorithm has its own tests. To run them, open the respective algorithm folder, and click on one of the batch scripts file to run a test. Upon clicking on the .bat file, the program will call the executable file passing the associated .csv files with it.

- Upon completing the script, you will see that a new .csv output file has been created in the same folder for the respective test case.

OTHER TESTS:
- If you wish to further test this program, follow the steps below:
	1) You may start by creating your own .csv files that follow the same format as shown in the other .csv files for the respective algorithm's folder. Upon creating the .csv files, name them and store them in the same directory with the rest of the files.
	2) create a .bat file that follows the same format as shown in the other .bat files for the respective algorithm's folder. The format of the .bat file must follow this order:
		To run a test case from the schedulers algorithms:
		- ExecutableFileName.exe newCsvfileName.csv 0 > outputFileName.csv

		To run a test case from the memory management algorithm, update the third argument:
		- ExecutableFileName.exe newCsvfileName.csv 0 0 > outputFileName.csv - If you want to run using the first partition discussed.
		- ExecutableFileName.exe newCsvfileName.csv 0 1 > outputFileName.csv - If you want to run using the second partition discussed.


