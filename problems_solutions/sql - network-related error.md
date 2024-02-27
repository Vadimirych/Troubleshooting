# SQL - A network-related or instance-specific error occurred while establishing a connection to SQL Server

## Error
TITLE: Connect to Server
------------------------------

Cannot connect to myserver.domain.com\SQLEXPRESS.

------------------------------
ADDITIONAL INFORMATION:

A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: SQL Network Interfaces, error: 26 - Error Locating Server/Instance Specified) (Microsoft SQL Server, Error: -1)

For help, click: https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver--1-database-engine-error

------------------------------
BUTTONS:

OK
------------------------------

## Solution 1
Check that correct instance name (myserver.domain.com\myinstance) is used or remove instance name from server name completely

## Solution 2
Check if port 1433 is open
1. Open SQL Server Configuration Manager on sql server machine
2. Choose SQL Server Network Configuration in the tree, not 32 bit
3. Protocols for SQLExpress
4. Enable TCP/IP
5. Open the TCP/IP Properties form.
6. Expand the IPALL group in the TCP/IP Properties form> IP addresses tab and enter “1433” in the TCP port field.
7. Restart SQL Server
