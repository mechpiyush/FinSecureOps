KEY FEATURES: 
1. VIEW TRANSACTIONS B/W TWO DATES, 
2. ARCHIVE TXNS, 
3. SEND EMAIL REPORT WITH KPIs LIKE SPEND IN LAST 1 YEAR, AVG SPEND

		View Transactions
		-> Client ID?
		-> Start Date*
		-> End Date*
		->
		-> Pull Credit		-> Pull Debit

--view of txns:	Txn id, Txn Date, Txn_type (CR/DB), Txn_Amount, Txn Status

MAJOR TASKS:				
1. MySQL
	1. CREATE THE DATA DUMP : DONE
	2. SCHEMA (Required tables: Txn, Txn_archive, Txn_archive_logs)
	3. Txn_archive: pulls the data from txn which is 1+ yrs old, and append it to Txn archive table.
	4. Txn_archive_logs: Stores the data for txn_archive operations with time stamps.
2. Bash
	1. Automate the scripts. 
	2. Cronjob if required.
	3. Whiptails UI.					
3. Email
	1. Sending bot msg or email report.
						
Plan to go with...
-> Schema for tables (ER diagram).
-> Data (done).
-> Txn pull script.
-> Txn_archive_log write operation log whenever we hit txn pull.  

I rest my case!!
