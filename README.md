<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Windows App
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Explore the osTicket portal.
- Administrating osTicket
- Configure Roles(Grouping Permissions)
- Configure Departments(Ticket Visibility, Help Desk vs SysAdmin vs Networking)
- Configure Teams(Pull Agents from Different Departments)
- Configure Agents(Workers)
- Configure Users(Customers)
- Configure SLA
- Configure Help Topics


<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/wAxjrjk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  <h3>Accessing osTicket Panels</h3>
<ol>
            <li>Open a web browser on your virtual machine (VM).</li>
            <li>Copy and paste the following links into your browser to access the required panels.</li>
            <li>The <strong>Admin/Agent Panel</strong> allows you to manage agents, departments, roles, tasks, and users.</li>
            <li>Access the Admin/Analyst Login Page: <strong>http://localhost/osTicket/scp/login.php</strong></li>
            <li>The <strong>User Panel</strong> is used to submit and track support tickets for IT helpdesk assistance.</li>
            <li>Access the User Login osTicket URL: <strong>http://localhost/osTicket</strong></li>
            <li>Ensure that both links are accessed within the VM’s browser before starting the configuration.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/9qCTu0U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>Assigning Roles in osTicket</h3>
        <ol>
            <li>Go to the <strong>Admin Panel</strong> in osTicket.</li>
            <li>Navigate to <strong>Agents</strong> and select <strong>Roles</strong>.</li>
            <li>Within each access section, assign specific <strong>roles</strong> to <strong>users</strong> or <strong>departments</strong>.</li>
            <li>For example, create a new role called <strong>"Supreme Admin"</strong>.</li>
            <li>Select all checkboxes under <strong>Tickets</strong> and <strong>Tasks</strong> to grant full administrative access.</li>
            <li>Apply the changes to provide the selected role with the appropriate permissions.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/MV1ZMdR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>Creating a New Department in osTicket</h3>
        <ol>
            <li>Go to the <strong>Admin Panel</strong> in osTicket.</li>
            <li>Click on <strong>Agents</strong>.</li>
            <li>Click on <strong>Departments</strong>.</li>
            <li>Click <strong>"Add New Department"</strong>.</li>
            <li>Enter the required department details.</li>
            <li>Fill in the following fields:</li>
            <li><strong>Name</strong> (Enter the department name).</li>
            <li><strong>Parent</strong> (Select the appropriate parent department).</li>
            <li><strong>Type</strong> (Specify the department type).</li>
            <li><strong>SLA</strong> (Set the service level agreement).</li>
            <li>For this lab, enter <strong>"SysAdmin"</strong> as the department name.</li>
            <li>Set the parent department to <strong>"Top Level Department"</strong>.</li>
            <li>Click <strong>"Create Dept"</strong> to finalize the setup.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/1eyWQgj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>Creating and Managing Teams in osTicket</h3>
        <ol>
            <li>Go to the <strong>Admin Panel</strong> in osTicket.</li>
            <li>Click on <strong>Agents</strong>.</li>
            <li>Select <strong>Teams</strong>.</li>
            <li>Enter a <strong>team name</strong>.</li>
            <li>Set the <strong>status</strong> of the team.</li>
            <li>Assign <strong>team members</strong> if applicable.</li>
            <li>Click <strong>"Save Changes"</strong> to finalize the team setup.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/wLzBL1J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>Enable Ticket Creation for Unregistered Users</h3>
        <ol>
            <li>Go to the <strong>Admin Panel</strong> in osTicket.</li>
            <li>Click or hover over <strong>Settings</strong>.</li>
            <li>Select <strong>Users</strong>.</li>
            <li>Scroll to the <strong>Authentication Settings</strong> section.</li>
            <li>Ensure the checkbox next to <strong>"Require registration and login to create tickets"</strong> is <strong>unchecked</strong>.</li>
            <li>Click <strong>"Save Changes"</strong> to apply the configuration.</li>
        </ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/YZmgCOA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h3>Adding a New Agent in osTicket</h3>
        <ol>
            <li>Go to the <strong>Admin Panel</strong> in osTicket.</li>
            <li>Click on <strong>Agents</strong>.</li>
            <li>Select <strong>Add New Agent</strong>.</li>
            <li>Under the <strong>Account</strong> tab, enter the following details:</li>
            <li><strong>First Name</strong></li>
            <li><strong>Last Name</strong></li>
            <li><strong>Username</strong></li>
            <li><strong>Email Address</strong></li>
            <li>Set Password by click <strong>Set Password</strong> and then uncheck <strong>Send the agent a password reset email</strong></li>
            <li>Go to the <strong>Access</strong> tab.</li>
            <li>Assign the agent to a <strong>Department</strong>.</li>
            <li>Select a <strong>Role</strong> for the agent.</li>
            <li>Go to the <strong>Teams</strong> section.</li>
            <li>Assign the agent to a <strong>Team</strong> if applicable.</li>
        </ol> 
</p>
<br />

<p>
<img src="https://i.imgur.com/ogw360a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  <h3>Adding a New User</h3>
<ol>
    <li>Navigate to the <strong>Agent Panel</strong>.</li>
    <li>Select the <strong>Users</strong> tab.</li>
    <li>Click <strong>Add User</strong>.</li>
    <li>Enter the required details:
        <ol>
            <li>First and last name</li>
            <li>Username</li>
            <li>Phone number</li>
        </ol>
    </li>
    <li>Click <strong>Add User</strong> to complete the process.</li>
</ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/S0SpLQY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <h3>Creating a New SLA Plan</h3>
<ol>
    <li>Navigate to the <strong>Admin Panel</strong>.</li>
    <li>Select the <strong>Manage</strong> tab.</li>
    <li>Under the <strong>Manage</strong> tab, click on <strong>SLA</strong>.</li>
    <li>Click <strong>Add New SLA Plan</strong>.</li>
    <li>For this lab, create the following SLA plans:
        <ol>
            <li>Sev-A</li>
            <li>Sev-B</li>
            <li>Sev-C</li>
        </ol>
    </li>
    <li>For each SLA, enter the required details:
        <ol>
            <li>Name</li>
            <li>Status</li>
            <li>Grace Period</li>
            <li>Schedule</li>
        </ol>
    </li>
    <li>Click <strong>Add Plan</strong> to finalize the creation.</li>
</ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/dpj4EGa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  <h3>Creating Help Topics for Users</h3>
<ol>
    <li>Navigate to the <strong>Admin Panel</strong>.</li>
    <li>Select the <strong>Manage</strong> tab.</li>
    <li>Under the <strong>Manage</strong> tab, click on <strong>Help Topics</strong>.</li>
    <li>Click <strong>Add New Help Topic</strong>.</li>
    <li>Enter the required details:
        <ol>
            <li>Name</li>
            <li>Status</li>
            <li>Type</li>
            <li>Parent Topic</li>
        </ol>
    </li>
    <li>Click <strong>Add Topic</strong> to complete the process.</li>
</ol>
</p>
<br />

