# Assignment II: Oracle PDB Management and OEM Setup

## Assignment Scope
This assignment covers multi-faceted aspects of Oracle 21c configuration, including:
* Creation and deletion of Pluggable Databases (PDBs)
* User creation and management inside a PDB
* Usage of Oracle Enterprise Manager (OEM)

## Task 1: Create a New Pluggable Database
**Steps**
* Log in to the Oracle database as sys admin user  
* Check the current CDB I am connected to using SHOW CON\_NAME;  
* Ideally, I will conventionally create the PDB inside CDB$ROOT and a local user connected to the PDB  
* Then, I will open the PDB and save its state so that I can read and write to it.

![](./images/image4.png) 

***Explanation of PDB creation***
```sql
-- create PDB
CREATE PLUGGABLE DATABASE da_pdb_20251sen104
-- create local user within PDB
ADMIN USER da_plsqlauca_20251sen104 IDENTIFIED BY admin
-- instruct Oracle where to store the pdb's data files
FILE_NAME_CONVERT=
('C:\APP\HP\PRODUCT\21C\ORADATA\XE\PDBSEED\',
 'C:\APP\HP\PRODUCT\21C\ORADATA\XE\da_pdb_20251sen104\');
```
