# Oracle Pluggable Databases (PDB) Management

**Course:** Database Development with PL/SQL (INSY 8311) 

**Student Name:** Bonheur TUYIRINGIRE

**Student ID:** 28824 

**Instructor:** Eric Maniraguha 

---

## 1. Overview of Tasks

This repository contains the documentation and evidence for Individual Assignment II. The primary objectives were:

* Implementing Oracle Multitenant Architecture.


* Managing the lifecycle of Pluggable Databases (Creation and Deletion).


* User administration within a specific PDB container.


* Monitoring the environment using Oracle Enterprise Manager (OEM).


## 2. Oracle Environment Used

**Database:** Oracle Database 21c (Multitenant Architecture).
* **Operating System:** Windows 11.
**Tools:** SQL*Plus, Oracle SQL Developer, and Oracle Enterprise Manager (OEM).


## 3. Task Documentation

### Task 1: Create a New Pluggable Database

<img width="589" height="401" alt="PDB CREATION (1)" src="https://github.com/user-attachments/assets/925e5700-5635-4911-a2a4-d0a10270e968" />


**PDB Name:** `bo_pdb_28824`.

**User Created:** `bonheur_plsqlauca_28824`.

**Process:** I created the PDB from the seed, opened it to a `READ WRITE` state, and established a local user with `CONNECT` and `RESOURCE` roles for future classwork.


### Task 2: Create and Delete a PDB
<img width="874" height="317" alt="CREATE AND DELETE PDBS" src="https://github.com/user-attachments/assets/109e64df-ef9a-4e2d-9da5-02e9650740ae" />

**Temporary PDB Name:** `bo_to_delete_pdb_28824`.

**Process:** I created a secondary PDB to demonstrate administrative control. After verifying its existence, I performed a complete deletion including datafiles to maintain system storage efficiency.


### Task 3: Oracle Enterprise Manager (OEM)

<img width="932" height="468" alt="OEM DASHBOARD" src="https://github.com/user-attachments/assets/5d40ad6c-f121-4262-9b4b-adb03538efb9" />  <img width="907" height="442" alt="OEM DASHBOARD 2" src="https://github.com/user-attachments/assets/15ce0656-ace9-4a77-97dc-5d776d94bf35" />


* I configured and accessed the OEM dashboard to monitor the database health.

* The dashboard reflects the active state of `bo_pdb_28824` and confirms the successful execution of administrative tasks.


## 4. Challenges Faced and Solutions

* **Challenge (ORA-00922):** Encountered a "missing or invalid option" error due to a period in the password.
* **Solution:** Enclosed the password in double quotes (`"..."`) to allow special characters.


* **Challenge (ORA-65040):** Attempted to create a PDB while already inside another PDB.
* **Solution:** Switched the session back to the root container using `ALTER SESSION SET CONTAINER = CDB$ROOT;`.

* **Challenge (ORA-01537):** File conflict error when creating the temporary PDB.
* **Solution:** Modified the `FILE_NAME_CONVERT` path to point to a unique folder for the new PDB.

## 5. Submission Details

**Repository Link:** [Insert your GitHub URL here] 
 
**PDB Name Created:** `bo_pdb_28824` 
 
**Issues Encountered:** Yes (Solved) 

## 6. Integrity Statement

I certify that this is a mandatory individual practical assignment. I have performed all tasks individually and have not copied commands or screenshots from any external sources or classmates. This work reflects my own execution and documentation.
