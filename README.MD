# PL/SQL Assignment II – Oracle Pluggable Database (PDB)

**Student Name:** Docile Uwizeye  
**Student ID:** 27549  
**Course:** PL/SQL  

---

## Executive Summary

This assignment demonstrates practical skills in Oracle Multitenant Database Administration, focusing on:

- Creating and managing Pluggable Databases (PDBs)  
- Handling the full PDB lifecycle (create, open, close, drop)  
- Monitoring databases using Oracle Enterprise Manager Express (EM Express)  

---

## Tasks Completed

### Task 1: Create Permanent PDB
- Created permanent PDB: `do_pdb_27549`  
- Created admin user: `docile_plsqlauca_27549`  
- Granted roles: `CONNECT`, `RESOURCE`, `DBA`, `UNLIMITED TABLESPACE`  
- Verified using:  
  - `v$pdbs` to confirm PDB is open  
  - `dba_users` to confirm user creation  
- Configured PDB to auto-open at startup  

**Screenshots / Verification:** 
![alt text](<Screenshot 2025-10-08 124311.png>)
- PDB is in `READ WRITE` mode  
- User successfully created  

---

### Task 2: Create & Delete Temporary PDB
- Created temporary PDB: `do_to_delete_pdb_27549`  
- Opened and verified using `v$pdbs`  
- Closed and dropped using `INCLUDING DATAFILES`  
- Verified only permanent PDB remains  

**Screenshots / Verification:**  
- Temporary PDB created  
- Both PDBs displayed  
- Drop command executed  
- Temporary PDB deleted  
- Only permanent PDB remains  

---

### Task 3: Configure Enterprise Manager Express (EM Express)
- Enabled HTTPS port `5500`  
- Logged in as `SYSDBA`  
- Verified:  
  - Configuration → Pluggable Databases → `do_pdb_27549` in OPEN state  
  - Security → Users → `docile_plsqlauca_27549` listed  
  - PDB details page accessible and functional  

---

## Issues & Solutions

| Issue | Solution |
|-------|---------|
| Port Conflict | EM Express was already using port 5500 → reused it |
| Wrong Container Context | Ran command in CDB accidentally → corrected with `ALTER SESSION SET CONTAINER` |

---

## Conclusion

- **PDB Management Mastered:** Created, opened, and dropped pluggable databases  
- **User Setup Understood:** Created users, granted roles, and configured quotas  
- **OEM Express Monitored:** Successfully logged in, verified users, and viewed performance  

The permanent PDB `do_pdb_27549` is fully functional and ready for PL/SQL coursework and future database administration exercises.

**Docile Uwizeye**  
**Student ID:** 27549



