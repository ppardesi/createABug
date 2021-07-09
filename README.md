# Utility for createABug:
It Creates a bug automatically in azure devops for failed test cases with the help of Azure Devops Rest api calls.

### Purpose:
This powershell script will solve the problem of creating bugs automatically in your azure devops pipeline, only if there are any failed test scenario during your last run.

### What to do:
You need to add a powershell task for your agent, to run a powershell script after publishing your test results.
1. Choose type - **Add this file to the file path**
2. Specify control options - **Set Run this task to: Even if a previous task has failed, unless the build was canceled**
3. Also allow your agent for OAuth token - **Allow scripts to access the OAuth token**

### What to configure
1. Below variables you need to configure to run this script
    * $orgUrl = "{Your Organisation}" - "https://dev.azure.com/ProjectName"
    * $personalToken = "{Your Personal Access Token - PAT}"
2. While creating a bug you need to input these fields as well
    * $workitemType = {"WorkItem Type as Bug"}
    * $Area = "{Your Project Area Path}"
    * $AssignedTo = "{Information of Assignee}"
    * $Reason = "{Reason}"
    

