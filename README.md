<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# <h1>osTicket - Post-Install Configuration</h1>

This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket and immediately follows the tutorial on [osTicket: Prerequisites and Installation](https://github.com/mcgregorsa/osticket-prereqs).

<br />



## <h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

## <h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

## <h2>Post-Install Configuration Objectives</h2>

- Define Roles. Departments, and Teams
- Set Ticket Creation Permissions and Create Agents and Users
- Configure SLA and Help Topics

## <h2>Configuration Steps</h2>
### <h3>Define Roles, Departments, and Teams</h3>

- In the Admin Panel.
  - Go to Agents Tab.
  - Select the Roles section.
  - Click Add New Role
    - Name the Role: Supreme Admin
    - Go to the Permissions Tab and check all the boxes in the Tickets, Tasks, and Knowledgebase Tabs.
    - Click Add Role

<p>
<img src="https://github.com/user-attachments/assets/a6315b9a-8cc8-4913-a531-07e7b689f70b" height="80%" width="80%" alt="Define Roles"/>
</p>
<br />

- Click the Departments section.
  - Click Add New Department
    - Name: SysAdmins
  - Click Create Department
  - Check the box for the Maintenance Department.
    - In the drop down arrow of the More button select Delete.
      - Do not Archive, Delete the Department.

<p>
<img src="https://github.com/user-attachments/assets/e9bd0e13-f701-4a3a-93e0-6bc3c9f2e19b" height="80%" width="80%" alt="Define Departments"/>
</p>
<br />

- Click the Teams Section.
  - Name: Online Banking
  - Click Create Team
  
<p>
<img src="https://github.com/user-attachments/assets/0684ee1a-bf53-4ba8-825b-3a7b1f93c2a2" height="80%" width="80%" alt="Define Teams"/>
</p>
<br />

### <h3>Set Ticket Creation Permissions and Create Agents and Users</h3>

- In the Settings Tab of the Admin Panel.
  - Go to Users
    - Under Registration Required:
      - Ensure the checkbox for "Require registration and login to create tickets" is checked.
  - Click Save Changes

<p>
<img src="https://github.com/user-attachments/assets/cb93ff53-b74a-4a3c-a997-c9ca184d67d8" height="80%" width="80%" alt="Require User Registration to Create Tickets"/>
</p>
<br />

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

<p>
<img src="https://github.com/user-attachments/assets/4f4db5d9-d345-4f52-b0ee-c84f10b2b6ed" height="80%" width="80%" alt="Create Agent Jane Doe"/>
</p>
<br />

- Log out and login as Jane Doe
  - Go to the Users Tab of the Agent Panel
    - Click Add User
      - Name: Karen Tyrell
      - email: karent@tyrellcorp.com (fake)
      - Register the user and uncheck that the password does not have to be changed on next login.

<p>
<img src="https://github.com/user-attachments/assets/37897309-96ff-4e05-886d-f47c95c18a6d" height="80%" width="80%" alt="Create User Karen"/>
</p>

<br />

### <h3>Configure SLA and Help Topics</h3>

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

<p>
<img src="https://github.com/user-attachments/assets/2f964639-4076-4780-a967-642fd3da52fe" height="80%" width="80%" alt="Create SLAs"/>
</p>
<br />

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
<img src="https://github.com/user-attachments/assets/5a73e333-f671-49b1-b08c-3a22d31c404c" height="80%" width="80%" alt="Create Help Topics"/>
</p>
<br />
