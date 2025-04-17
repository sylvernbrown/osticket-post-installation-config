<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Installation Configuration (2/3)</h1>
In this demonstration, we’ll dive into the post-installation configuration of osTicket, a widely used open-source help desk ticketing system.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- osTicket: Admin & Agent Control Panels

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Virtual Environment & Administrator Login
- Agent Role Configuration
- Department Configuration
- Team Configuration
- Creating Agents & Delegating Permissions
- Creating Users
- Creating Service Level Agreement (SLA) Plans6
- Creating Help Topics

<h2>Configuration Steps</h2>

<p>
1) Log into your virtual machine, then navigate to the osTicket <strong>Admin Login</strong>.  
  '

  http://localhost/osTicket/scp/login.php
  
'
</p>
<br />
<p>
<img src="https://i.imgur.com/Ymjn29b.png" height="60%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />

<p>
2)To modify an Agent's role, from the <strong>Admin Panel</strong>, navigate to <strong>Agents > Roles</strong>. Select <strong>"Add a New Role"</strong>, in the example below I set the name as <strong><i>Supreme Admin</strong></i>.  This role will be the highest administrative role, so I allowed all permissions.  I recommend having at least one role with all permissions, for accessibility to osTicket functions. <br />
  
<strong>Roles Info</strong>: Roles are permissions assigned to individual agents.  For example, an agent with "Limited Access" may only be able to view whereas a "Supreme Admin" may have access to viewing, editing, closing tickets, etc.
  <br />
  <br />
    <strong><i>Note: If you are unable to access osTicket or modify tickets as an agent later on in this process, it's likely that the user you're logged in as isn't permitted access.</i></strong>

</p>
<br />
<p>
<img src="https://i.imgur.com/WxomJMn.png" height="60%" width="80%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/9oA9yPA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />

<p>
3) Configure Departments by navigating to <strong>Admin Panel > Agents > Departments</strong>.  When creating your top-level department, name it anything that fits the roles of your organization but be sure to select the <strong>Top-Level Department</strong> setting under <strong>Parent</strong> as shown below or else your department won't be able to access advanced ticket settings in the admin panel.<br/>
  <br/>
<strong><u>Department Info</u></strong>: Department permissions allow groups of specialists to have access to tickets based on their work-groups. More specifically, <strong>Parent Departments </strong>  are managerial  and <strong>Child Departments </strong>  are subordinate. Agents in <strong>Parent Departments</strong> can see all open tickets while agents in <strong>Child Departments</strong> only can see their own tickets.</strong><br />
  </p>
<br />
<p>
<img src="https://i.imgur.com/PVvenlK.png" height="60%" width="80%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/kl1jHiI.png" height="60%" width="80%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />

<p>
4)To setup a team,  navigate to <strong>Admin Panel > Agents > Teams</strong>.  Select <strong>"Create New Team"</strong> and name it. Once your team is named, it should appear in the Admin Panel as shown below. <br/>
  <br />
<strong>Team Info</strong>: Teams allow agents from different departments to have similar permissions for any given task or project.  For example, there may be a team dedicated to a specific product or service like mobile orders that require specialized agents from different departments.<br 
</p>
<br />
<p>
<img src="https://i.imgur.com/Q5Kr7Fk.png" height="60%" width="80%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/lzHH7MJ.png" height="60%" width="80%" alt="Disk Sanitization Steps"/><br/>
</p>
  <br />
  <br />
  <br />
  <br />

5)<strong>(Optional) Requiring Registration & Login to Create Tickets</strong>: Navigate to <strong>Admin Panel > Settings > User Settings</strong>.  Check the box that says <strong>"Require registration and login to create tickets"</strong>.<br />
<br />
<img src="https://i.imgur.com/f67gAfk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
  <br />
  <br />
  <br />
6) <strong>Creating Agents</strong>: Navigate to <strong>Admin Panel > Agents, select "Add New"</strong>.  Create as many agents as desired, for demonstration purposes I added two agents John & Jane.  I assigned one to <strong>Support</strong> and another to the <strong>SysAdmins department</strong>.  As you can see below, this is where you can assign your agents to departments.<br />
<br />
<img src="https://i.imgur.com/zjD4D83.png" height="60%" width="80%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/y5XUZvl.png" height="60%" width="80%" alt="Disk Sanitization Steps"/><br/>
<p>
  <br />
  <br />
  <br />
7) <strong>To create new Users:</strong> Navigate to the <strong>Agent Panel</strong> in the top right hand corner of osTicket, navigate to users and select <strong>"Add New"</strong>.  Add as many users as desired, please see demonstration below. <br />
  <br />
</p>
<br />
<p>
<img src="https://i.imgur.com/CQpXOL1.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/7QJbFnP.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
  <br />
  <br />
  <br />
  <br />

<p>
8) <strong>To setup a new series of SLA Plans:</strong> Navigate to <strong>Admin Panel > Settings > Tickets</strong>.  Please see the demonstration below. <br />
<br />
<strong>SLA Plans Info</strong>: SLA Plans or Service Level Agreements are subjective time metrics set by an organization or desk administrator to communicate when they expect a ticket to be closed.<br />
<br />
</p>
<br />
<p>
<img src="https://i.imgur.com/pLy5kEA.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
  <br />
  <br /> 
<strong><i>Note: Notice the relevant categories when considering ticket settings.  Default status, default priority, default SLA, and default help topic seem to be the most common modifications. There are also more advanced settings such as CAPTCHA requirements and ticket formatting settings.</i></strong><br />
  <br/>
<img src="https://i.imgur.com/gRXcRoe.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
  <br />
  <br /> 
<strong><i>Note: Below is an example of an SLA conifguration you could possibly arrange.</i></strong><br />
  <br />
<img src="https://i.imgur.com/EttuRAP.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
  <br />
  <br />
  <br />
  <br />


<p>
9) <strong>To add Help Topics:</strong> Navigate to <strong>Admin Panel > Manage > Help Topics</strong>.  Then, add a few topics, some examples may include: <strong>Business Critical Outage, Equipment, Password Reset, Personal Computer Issues, etc.</strong><br />
  </p>
<br />
<strong>SLA Help Topics Info</strong>: Help Topics are user-selected topics they believe most accurately describe the issues they're experiencing.  Adding a wide variety of topics can allow for better differentiation between departments of various technical issues.<br />
<br />
<p>
<img src="https://i.imgur.com/Gags2Lz.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
  <br />
  <p><strong><i>Note: After you setup relevant help topics, they should appear here afterwards.  You can track the status, time, department, and more from this panel</i></strong></p><br />
  <br />
<img src="https://i.imgur.com/1hfsCQa.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
  <br />
  <br />
  <br />
  <br />



