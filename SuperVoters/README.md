# SuperVoters

This is a group project for WSU Cpts583.

# Team Info

| Team Name          | SuperVoters                                        |
| ------------------ | -------------------------------------------------- |
| Project topic      | Electronic Voting System                           |
| Project repository | https://github.com/leiawang89/SuperVoters |

| Team Info    | Name              | Email                     | WSU ID    | GitHub       | Contact |
| ------------ | ----------------- | ------------------------- | --------- | ------------ | ------- |
| Team members | Garhgajpal Singh  | garhgaj.singh@wsu.edu     | 011470057 | gargi79      |         |
|              | David Kelly       | david.e.kelly@wsu.edu     | 011779437 | davidke1234  |         |
|              | Ya Wang           | ya.wang@wsu.edu           | 011672796 | leiawang89   | Yes     |
|              | Jonathan Coronado | jonathan.coronado@wsu.edu | 011541511 | MacMuffin117 |         |

# Getting Started

How to use the Voting System
1.  Install the application
2.  To gain access, send your public IP address to the Admin. 
    - To find your public IP address use Bing search: what's my ip address site:microsoft.com
3.  Run the application
	See doc on git hub.  


# Developer details:

# Tools

    1. Visual Studio 2019
    2. Git for windows
    3. Windows Forms development
	4. Azure SQL

# Setup

    1. Install Visual Studio 2019.
    2. Install Azure Data Studio - https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15#download-azure-data-studio
	   a. Setup a new Connection
		   - Server: tcp:supervoters.database.windows.net, 1433
		   - UserName: supervotersadmin
		   - Password: See connection string
		   - Database: SuperVoters
    3. Install Git: https://git-scm.com/download/win.
    4. Clone the repository using HTTPS. Copy url to buffer.
    5. Create project directory folder C:\WSUProjects\583\
    6. Run git clone from your project directory: git clone url.
    	
# Change Process using Git

    1. Add files to the project dir or modify them.
    2. Get the status: git status.
    3. Run git add to stage files for commit: git add.
    4. Commit files: git commit -m "message".
    5. Push files to repo: git push.

    Optionally use Visual Studio git.

# Logging using LogFactory (nLog)
2. Add a call to LogFactory to catch blocks or anywhere.  LogLevels are Error, Info, Debug, Trace, Warn
    - catch (Exception ex)
        {
            LogFactory.WriteLog(LogFactory.Level.Error, "An error occurred: " + ex.Message);
        }
        LogFactory.WriteLog(LogFactory.Level.Info, "A new voter was created: " + voterId);
4. The logger will log to a file locally:
    - SuperVoters\bin\Debug\Logs
5. The logger will log to SQL Server
    - SELECT TOP (1000) [Id]
      ,[CreatedOn]
      ,[Level]
      ,[Message]
      ,[StackTrace]
      ,[Exception]
      ,[Logger]
      ,[Url]
    FROM [dbo].[Logs]

 

