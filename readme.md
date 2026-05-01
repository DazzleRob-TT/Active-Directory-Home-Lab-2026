# Active Directory Home Lab 2026

## **Introduction**

This is a basic home lab of Active Directory that I attempted using Windows Server 2022.

## What I used to do the lab

Virtualization Software: VMware Workstation 25H2

Operating systems: Windows Server 2022 and Windows 10

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd60db98b1d0d9f3a17065ecb6fb57c933f6863/Phase%201/IP%20Change1.png)

Select Ethernet0 in the Local Sever Tab, IPv4 address assigned by DHCP, IPv6 enabled.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/704d0fe3d5524a10f6adbe961b5c16807e1e30d3/Phase%201/IP%20Change%202.png)

Right click Interface select properties.

Select Internet Protocol Version 4 (TCP/IPv4) then select properties.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/16ffa733b182ad3097bce2b2629bde3aa5aa7407/Phase%201/IP%20Change%203.png)
Select use the following IP address.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/16ffa733b182ad3097bce2b2629bde3aa5aa7407/Phase%201/IP%20Change%204.png)

Enter the IP address, subnet mask, and default gateway.

At the bottom select use the following DNS server addresses.

In the preferred DNS server field enter the DNS server (I used the loopback IP address) and select OK.

# **Changing the computer name**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/3d7e41e023f40a0ff12c923eb9ca446f03d85f0e/Phase%201/Change%20name%201.png)

Go to Server Manager then to Local Server. 

Select the computer name.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%201/Change%20name%202.png)

Select change.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/main/Phase%201/Change%20name%203.png)

Enter the computer name (DC1) and select OK.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/3d7e41e023f40a0ff12c923eb9ca446f03d85f0e/Phase%201/Change%20name%204.png)

Select OK and restart the virtual machine.

# **Installing roles (AD DS, DHCP, DNS)**

Go to Server Manager.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/Adding%20roles%20p1.png)

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%202.png)

Select Manage> Add Roles and Features.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%203.png)

The Add Roles and Features Wizard will appear.

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%204.png)

Select Role Based or feature-based installation and select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%205.png)

There is one server, select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%208.png)

For the server roles select Active Directory Domain Services, DHCP Server and DNS Server.

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%207.png)

Select Add Features.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%209.png)

In the Features section ensure Group Policy Management is ticked and select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%2010.png)

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2011.png)

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2012.png)

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2013.png)

Select install.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2014.png)

Wait for the installation to complete.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2015.png)

After the installation is completed select promote this server to a domain controller.

# **Server promotion to a Domain Controller**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%202.png)

Select add a new forest and enter the root domain name.

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%203.png)

Select a a functional forest and domain level.

Enter a Directory Services Restore Mode password.

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%204.png)

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%205.png)

A NETBIOS name will be generated.

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%206.png)

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%207.png)

Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%208.png)

Select install.

The server will be restarted and the server will be become a domain controller.

# **Creating users and groups in Active Directory**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/Users%20and%20groups%201.png)

Go to Server Manager then Tools select Active Directory Users and Computers.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%202.png)

Select the domain drop down. 

In the right pane section right click. 

Go to New>Organizational Unit

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%203.png)

Enter a name. 

Select OK.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%204.png)

I made another Organizational Unit within the previous one and named it “Users”.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%205.png)

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%206.png)

Within the Users Organizational Unit I made a Group called Admin Department.

# **Creating a User**

![alt image]()

In the right pane section right click. 

Go to New>User.

![alt image]()

Enter the user credentials.

Select next.

Create a user password.

For the purposes of this lab I checked the Password never expires box.

Select Finished.

![alt image]() 

The user is now created.

## **Adding a user to a group**

![alt image]()

Right click a user.

Select add to a group.

![alt image]()

Enter the name of the group in the white section. 

Select check names.

![alt image]()

The group was found successfully indicated by the underline.

Select OK.

![alt image]()

Select OK.

![alt image]()


To verify what groups a user is a member of
right click the user>select the member of tab.

# **DHCP Scope Configuration**
## DHCP after role installation

Run the DHCP Post-Install configuration wizard to authorize the DHCP server and press Commit. 

I Forgot to do this before configuring the DHCP Scope.

![alt image]()

Go to Server manager>Tools>DHCP.

![alt image]()

Right click IPv4>Select New Scope.

![alt image]()

Select next.

![alt image]()

Give the scope a name.

Select next.

![alt image]()

Enter the IP address range for the scope along the with the length and subnet mask.

Select next.

![alt image]()

Add any IP address exclusions.

Select next.

![alt image]()

Enter the lease duration of an IP address.

Select next.

![alt image]()

Select “Yes I want to configure DHCP options now”.

Select next.

![alt image]()

Add an IP address for the default gateway.

Select next.

![alt image]()

Select next.

![alt image]()

Select next.

![alt image]()

Select “Yes, I want to activate this scope now”.

Select next.

![alt image]()

Select finish.

# **Adding a computer to the domain**

Sign into pc.

![alt image]()

Search for and click control panel.

![alt image]()

Select network and internet.

![alt image]()

Select network and sharing center.

![alt image]()

Select change adapter settings.

![alt image]()

Right click the adapter>Select properties.

![alt image]()

Select Internet Protocol Version 4 (TCP/IPv4).

Select properties.

![alt image]()

Give the pc an IP address to connect to the domain.

Select OK.

![alt image]()

I opened command prompt and entered the ipconfig /all command to verify the all the IP configuration information.

I then tested connectivity with the domain controller by doing a ping command.

The test results were successful in that the pc can communicate with the domain controller.

The next step is to add the pc to the domain.

![alt image]()

Right click the start button>Select system.

![alt image]()

Select advanced system settings.

![alt image]()

Select change.

![alt image]()

I renamed the computer to PC1.

Under member of select domain.

Enter the domain name and select OK.

![alt image]()

A prompt will appear to enter administrative privileges to add the computer to the domain.

Enter the administrative credentials and select OK.

![alt image]()

The computer was added to the domain.

The computer will be restarted.

![alt image]()

After the restart sign in as a domain user.

![alt image]()

I am now signed as a domain user.

![alt image]()

I configured the computer to receive a DHCP address.

![alt image]()

I confirmed that a DHCP address is in use by the doing the ipconfig /all command in command prompt.

# **Creating Group Policies**

![alt image]()

Go to the start menu of the domain controller and search for Group Policy Management.

Select Group Policy Management.

![alt image]()

![alt image]()

Select the domain and right click>Select “Create a GPO in this domain, and link it here”.

![alt image]()

Enter the name of the Group Policy Object. 

I am creating a password policy.

Select OK.

![alt image]()

To configure the policy right click the policy and select edit.

![alt image]()

To find the appropriate policy settings select computer configuration>policies>windows settings>security settings>account policies>password policy.

![alt image]() 

![alt image]()

I configured the policy.

![alt image]()

I also configured an account lockout policy.

After 4 invalid logon attempts an account will be locked.

![alt image]()

I placed the PC1 computer in a computers Organizational Unit that I created.

![alt image]()

I forced the group policies to be implemented on the client computer by inserting the gpupdate /force command in command prompt.

Testing the account lockout policy

Video of me testing the policy.

# **Creating a shared folder**

![alt image]()

Go to the domain controller and create a folder.

I created a folder in the C: drive.

![alt image]()

Right click the folder>Select properties

![alt image]()

Select the sharing tab>Select advanced sharing

![alt image]()

Select share this folder.

![alt image]()

Select permissions.

![alt image]()

This can be left as default.

Select OK.

![alt image]()

Within the shared folder I created a folder named “Admin Department”

Right click the folder and select properties.

![alt image]()

Select the sharing tab>Select share.

![alt image]()

Enter the name of the group to give permission to access the folder.

I entered “Admin Department” and selected add.

![alt image]()

I gave the group read/write permissions and selected share.

# **Mapping the share drive on the client machine**

![alt image]()

Go to the client machine and login as a domain user.

Go to “This PC” in the file explorer.

Go to the ribbon at the top and select “Map network drive”.

![alt image]()

I entered the server name “\\DC1” and selected browse.

![alt image]()

I selected the share folder and selected OK.

![alt image]()

Select finish.

![alt image]()

The drive was successfully mapped.

# **Testing the shared folder permissions**

![alt image]()

I navigated to the Admin Department folder and attempted to add a text document.

![alt image]()

The text document was added successfully and this means the read/write configuration worked.

# **Conclusion**
I learned that some policies in GPO can not be implemented at the OU level but has to be linked to the entire domain for example Password policies and account lockout policies are to be attached to the domain.

I plan to expand this home lab and continue to learn more about active directory.
