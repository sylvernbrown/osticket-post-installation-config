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
- Creating Service Level Agreement (SLA) Plans
- Creating Help Topics

<h2>Configuration Steps</h2>

<p>
1) Begin by logging into your virtual machine and accessing the osTicket <strong>Admin Panel</strong> (typically found at (http://localhost/osTicket/scp/login.php), then authenticate using the admin credentials you recorded during the <strong>osTicket Prerequisites installation</strong>.
  

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
2)To modify an agent's role, from the <strong>Admin Panel</strong>, navigate to <strong>Agents > Roles</strong>. Select <strong>"Add a New Role"</strong>, in this example I set the name as <strong><i>Supreme Admin</strong></i>.  This role will be the highest administrative role, so allow all permissions as shown below. <br />
  
<strong>Roles Info</strong>: Roles are permissions assigned to individual agents.  For example, an agent with "Limited Access" may only be able to view whereas a "Supreme Admin" may have access to viewing, editing, closing tickets, etc.
  <br />
  <br />
    <strong><i>Note: If you are unable to access osTicket or modify tickets as an agent later on in this process, it's likely that you didn't select all permissions when creating your admin role.</i></strong>

</p>
<br />
<p>
<img src="https://i.imgur.com/WxomJMn.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/9oA9yPA.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />

<p>
3) Configure Departments by navigating to <strong>Admin Panel > Agents > Departments</strong>.  When creating your top-level department, name it anything that fits the roles of your organization but be sure to select the <strong>Top-Level Department</strong> setting under <strong>Parent</strong> as shown below or else your department won't be able to access advanced ticket settings in the admin panel.<br/>
  <br/>
<strong><u>Department Info</u></strong>: Department permissions allow groups of specialists to have access to tickets based on their work-groups. More specifically, <strong>Parent Departments </strong>  are managerial departments and <strong>Child Departments </strong>  are subordinate departments. Agents in <strong>Parent Departments</strong> can see all open tickets while agents in <strong>Child Departments</strong> only can see their own tickets.</strong><br />
  </p>
<br />
<p>
<img src="https://i.imgur.com/PVvenlK.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/kl1jHiI.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />

<p>
<strong>Team Info</strong>: Teams allow agents from different departments to have similar permissions for any given task or project.  For example, there may be a team dedicated to a specific product or service like mobile orders that require specialized agents from different departments.<br />
  <br/>
4)To setup a team,  navigate to <strong>Admin Panel > Agents > Teams</strong>.  Select <strong>"Create New Team"</strong> and name it. Once your team is named, it should appear in the Admin Panel as shown below.
</p>
<br />
<p>
<img src="https://i.imgur.com/Q5Kr7Fk.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/lzHH7MJ.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />

5a)Now, we are going to begin the process of creating agents by navigating to Admin Panel > Settings > User Settings.  Check the box that says "Require registration and login to create tickets", ensuring only internal employees can access your osTicket ticketing portal.<br />
<br />
<img src="https://i.imgur.com/f67gAfk.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
<br />
5b)To create Agents, navigate to Admin Panel > Agents, select "Add New".  Create as many agents as desired, for demonstration purposes I added two agents John & Jane.  I assigned one to Support and another to the SysAdmins department.  As you can see below, this is where you can assign your agents to departments.<br />

<img src="https://i.imgur.com/zjD4D83.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
<img src="https://i.imgur.com/y5XUZvl.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>

5c) Finally, we are going to add in Users so they can access the osTicket support center.  Navigate to the Agent Panel in the top right hand corner of osTicket, navigate to users and select "Add New".  Add as many users as desired, please see demonstration below. 
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
<strong>SLA Plans Info</strong>: SLA Plans or Service Level Agreements are subjective time metrics set by an organization or desk administrator to communicate when they expect a ticket to be closed.<br />
<br />
6) To setup a new series of SLA Plans custom to your organization, navigate to Admin Panel > Settings > Tickets.  Please see the demonstration below. <br />
<br />
</p>
<br />
<p>
<img src="https://i.imgur.com/pLy5kEA.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
  <br />
  <br /> 
<i>Note: Notice the relevant categories when considering ticket settings.  Default status, default priority, default SLA, and default help topic seem to be the most common modifications. There are also more advanced settings such as CAPTCHA requirements and ticket formatting settings.</i>
<img src="https://i.imgur.com/gRXcRoe.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
  <br />
  <br /> 
<i>Note: The example provided below is a common example of how an organization might setup SLA configurations to optimize ticket efficiency and priority.  If you wish, you can copy this version rather than creating your own settings from scratch.</i>
<img src="https://i.imgur.com/EttuRAP.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />

<strong>SLA Help Topics Info</strong>: Help Topics are user-selected topics they believe most accurately describe the issues they're experiencing.  Adding a wide variety of topics can allow for better differentiation between departments of various technical issues.<br />
<br />
7) To add help topics, navigate to Admin Panel > Manage > Help Topics.  It should look something like this.  Add a few topics, some examples may include: Business Critical Outage, Equipment, Password Reset, Personal Computer Issues, etc.
  </p>
<br />
<p>
<img src="https://i.imgur.com/Gags2Lz.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
  <br />
  <p><i>Note: After you setup relevant help topics, they should appear here afterwards.  You can track the status, time, department, and more from this panel</i></p>
<img src="https://i.imgur.com/1hfsCQa.png" height="40%" width="60%" alt="Disk Sanitization Steps"/><br/>
</p>
<br />
<br />
<br />
<br />



