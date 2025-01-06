<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Configuration Steps</h2>
<h3>Define Roles. Departments, and Teams</h3>

- In the Admin Panel.
  - Go to Agents Tab.
  - Select the Roles section.
  - Click Add New Role
    - Name the Role: Supreme Admin
    - Go to the Permissions Tab and check all the boxes in the Tickets, Tasks, and Knowledgebase Tabs.
    - Click Add Role
- Click the Departments section.
  - Click Add New Department
    - Name: SysAdmins
  - Click Create Department
  - Check the box for the Maintenance Department.
    - In the drop down arrow of the More button select Delete.
      - Do not Archive, Delete the Department.
- Click the Teams Section.
  - Name: Online Banking
  - Click Create Team
  
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<h3>Set Ticket Creation Permissions and Create Agents and Users</h3>

- In the Settings Tab of the Admin Panel.
  - Go to Users
    - Under Registration Required:
      - Ensure the checkbox for "Require registration and login to create tickets" is checked.
  - Click Save Changes
- Go to the Agents Section of the Admin Panel.
  - Click Add New Agent
    - In the text fields fill in:
      - Name, Email, and Username
        - Name: Jane Doe
        - Username: JaneD
        - Use a fake email.
    - Click "Set Password" next to the Username text field.
      - In the "Set Agent Password" pop-up
        - Uncheck the "Send the agent a password reset email" and type in a password and confirm it in the text fields that open up.
    - In the Access Tab under Primary Department.
      - Set the dropdowns to SysAdmins and Supreme Admin, respectively.
    - In the Permissions Tab
      - Ensure all checkboxes are checked in the Users, Orgainizations, Knowledgebase, and Miscellaneous sections.
    - In the Teams Tab
      - Set the Assigned Teams dropdown to Online Banking.
    - Click Create
  - Repeat the Agent creation steps with the following differences.
    - Name: John Smith
    - Username: JohnS
    - Primary Department dropdowns
      - Support and All Access
- Log out and login as Jane Doe
  - Go to the Users Tab of the Agent Panel
    - Click Add User
      - Name: Karen Tyrell
      - email: karent@tyrellcorp.com (fake)
      - Register the user and uncheck that the password does not have to be changed on next login.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />
<h3>Configure SLA and Help Topics</h3>

- In the Admin Panel under the Manage Tab
  - Click "Add New SLA Plan"
  - In the formfields set the following:
    - Name: Sev-A
    - Grace Period: 1
    - Schedule: 24/7
  - Click "Add Plan"


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
