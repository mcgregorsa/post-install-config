<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
<p>
  This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket and immediately follows the tutorial on [osTicket: Prerequisites and Installation](https://github.com/mcgregorsa/osticket-prereqs)</p>

<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Define Roles. Departments, and Teams
- Set Ticket Creation Permissions and Create Agents and Users
- Configure SLA and Help Topics

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
  - Select the SLA Section
    - Click "Add New SLA Plan"
      - In the formfields set the following:
        - Name: Sev-A
        - Grace Period: 1
          - This is the time (in hours) after the ticket is created it will be marked as overdue if no response has been made.
        - Schedule: 24/7
          - This defines the timer for the grace period. A Business Hours schedule would not count the Grace Period outside of defined business hour, i.e. 9 am to 5 pm.
    - Click "Add Plan"
    - Add 2 more SLA Plans with the following
      - SLA Sev-B
        - Name: Sev-B
        - Grace Period: 4
        - Schedule: 24/7
      - SLA Sev-C
        - Name: Sev-C
        - Grace Period: 8
        - Schedule: Business Hours
- In the Admin Panel under the Manage Tab
  - Select the Help Topics Section
    - Click "Add New Help Topic"
      - In the formfields set the following:
        - Topic: Business Critical Outage
        - Parent Topic: Report a Problem
        - Under the New ticket options tab:
          - Priority: High
          - SLA Plan: Sev-A
      - Click "Add Topic"
    - The above can be repeated the following Help Topics and setting their Parent Topics, Priority, and SLA Plan appropriately based on the issue type:
      - Personal Computer Issues
      - Equipment Request
      - Password Reset
      - Other


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
