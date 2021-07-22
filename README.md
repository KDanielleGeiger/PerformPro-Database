# PerformPro Database

This repository contains the required database files for the PerformPro web application.
View the PerformPro repository here: [PerformPro](https://github.com/KDanielleGeiger/PerformPro)

## How to Use

Open SQL Server Management Studio (SSMS) and connect:
* Server Type: Database Engine
* Authentication: Windows Authentication

Move PerformPro.bak into the SSMS backup directory.
C: -> Program Files -> Microsoft SQL Server -> MSSQL15.SQLEXPRESS -> MSSQL -> Backup

Open SQLQuery.sql in SSMS, replace the string with the path to PerformPro.bak, and run to restore the database.


In Visual Studio:
* Open the PerformPro project
* Go to View -> Server Explorer and select Add Connection
* Select Microsoft SQL Server as the data source and .NET Framework Data Provider for SQL Server as the data provider. Hit OK
* Paste the server name (For example, DESKTOP-ABC1234\SQLExpress) into the Server Name field
* Under "Select or enter a database name", choose PerformPro. Hit OK


The server should appear under Data Connections in the Server Explorer now.
* Right-click the server and chooose Properties
* Find and copy the Connection String
* Open appsettings.local.json and paste the connection string, making sure to properly escape characters
* Save and close the file
* In Visual Studio, drag appsettings.local.json onto the PerformPro folder
* Run the application
