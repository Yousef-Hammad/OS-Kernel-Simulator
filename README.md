# OS-Kernel-Simulator

## Project Description
This project is simulates an ATM system using three concurrent processes:
1. An ATM interface that allows for user interaction, and provides authentication, balance checking, and withdrawal functionality
2. A Database Server that communicates with the ATM to fetch and store user account information
3. A Database Editor that communicates with the Database Server to create and update account information

## Project Structure
```
.
├── Makefile           - Includes compliation commands
├── README.md          - Project information (you are here!)
├── system_diagram.png - System diagram (shown the bottom of the README)
├── main.c             - The ATM code, also launches the DB Server
├── db_editor.c        - The DB Editor source code
├── db_server.c        - The DB Server source code
├── db.h               - Header file for the project, contains shared macros and data structures
├── db.csv             - The Database
├── main               - Executable, starts ATM and DB Server
├── db_editor          - Executable for the DB Editor
├── db_server          - Executable for the DB Server, started by `main`, DO NOT START DIRECTLY
└── db_key             - Key used by the Message Queues - do not touch
```

## Running the Project
**NOTE:** To quit at any time from the ATM or the DB Edtior, type `x`
To start the ATM, execute `main` on a Linux system or shell (this will also start up the DB Server)

```./main```

To start the DB Editor, execute `db_editor` on a Linux system or shell (make sure you've already started the ATM and DB Server)

```./db_editor```

or compile the source code yourself using the Makefile

```make```

for a regular build or

```make debug```

to include additional debug print statements. If you don't have make, run the compile commands directly with gcc, or another compiler of your choice.

```gcc main.c -o main && gcc db_server.c -o db_server && gcc db_editor.c -o db_editor```

## System Diagram
![The System Diagram of the ATM system](./system_diagram.png)

