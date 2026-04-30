# Active Directory Home Lab 2026

## **Introduction**

This is a basic home lab of Active Directory that I attempted using Windows Server 2022.

## What I used to do the lab

Virtualization Software: VMware Workstation 25H2

Operating systems: Windows Server 2022 and Windows 10

![image alt] (Image)

Select Ethernet0 in the Local Sever Tab, IPv4 address assigned by DHCP, IPv6 enabled

(Image)
Right click Interface select properties.

Select Internet Protocol Version 4 (TCP/IPv4) then select properties.

(Image)
Select use the following IP address.

Enter the IP address, subnet mask, and default gateway
At the bottom select use the following DNS server addresses

In the preferred DNS server field enter the DNS server (I used the loopback IP address) and select OK.

# **Changing the computer name**
image

Go to Server Manager then to Local Server. 

Select the computer name.

image

Select change.

image
Enter the computer name (DC1) and select OK.

image
Select OK and restart the virtual machine.

# **Installing roles (AD DS, DHCP, DNS)**

Go to Server Manager.

image

Select Manage> Add Roles and Features

image

The Add Roles and Features Wizard will appear.

Select next.

image


Select Role Based or feature-based installation and select next.

image

Select next.

image

For the server roles select Active Directory Domain Services, DHCP Server and DNS Server.

Select next.

image

Select Add Features.

image

In the Features section ensure Group Policy Management is ticked  and select next.

image

Select next.

image

Select next.

image

Select next.

image

Select install.

image

Wait for the installation to complete.

image

After the installation is completed select promote this server to a domain controller.

# **Server promotion to a Domain Controller**

image

Select add a new forest and enter the root domain name.

Select next.

image

Select a a functional forest and domain level.

Enter a Directory Services Restore Mode password.

Select next.

image

Select next.

image

A NETBIOS name will be generated.

Select next.

image

Select next.

image

Select next.

image

Select install.

The server will be restarted and the server will be become a domain controller.

# **Creating users and groups in Active Directory**

image

Go to Server Manager then Tools select Active Directory Users and Computers.

image

Select the domain drop down. 

In the right pane section right click. 

Go to New>Organizational Unit

image

Enter a name. 

Select OK.

image

I made another Organizational Unit within the previous one and named it “Users”.

image

image

Within the Users Organizational Unit I made a Group called Admin Department.

# **Creating a User**

image

In the right pane section right click. 

Go to New>User.

image

Enter the user credentials.

Select next.

Create a user password.

For the purposes of this lab I checked the Password never expires box.

Select Finished.

image 

The user is now created.

## **Adding a user to a group**

image

Right click a user.

Select add to a group.

image

Enter the name of the group in the white section. 

Select check names.

image

The group was found successfully indicated by the underline.

Select OK.

image

Select OK.

image


To verify what groups a user is a member of
right click the user>select the member of tab.

# **DHCP Scope Configuration**
## DHCP after role installation

Run the DHCP Post-Install configuration wizard to authorize the DHCP server and press Commit. 

I Forgot to do this before configuring the DHCP Scope.

image

Go to Server manager>Tools>DHCP.

image

Right click IPv4>Select New Scope.

image

Select next.

image

Give the scope a name.

Select next.

image

Enter the IP address range for the scope along the with the length and subnet mask.

Select next.

image

Add any IP address exclusions.

Select next.

image

Enter the lease duration of an IP address.

Select next.

image

Select “Yes I want to configure DHCP options now”.

Select next.

image

Add an IP address for the default gateway.

Select next.

image

Select next.

image

Select next.

image

Select “Yes, I want to activate this scope now”.

Select next.

image

Select finish.

# **Adding a computer to the domain**

Sign into pc.

image

Search for and click control panel.

image

Select network and internet.

image

Select network and sharing center.

image

Select change adapter settings.

image

Right click the adapter>Select properties.

image

Select Internet Protocol Version 4 (TCP/IPv4).

Select properties.

image

Give the pc an IP address to connect to the domain.

Select OK.

image

I opened command prompt and entered the ipconfig /all command to verify the all the IP configuration information.

I then tested connectivity with the domain controller by doing a ping command.

The test results were successful in that the pc can communicate with the domain controller.

The next step is to add the pc to the domain.

image

Right click the start button>Select system.

image

Select advanced system settings.

image

Select change.

image

I renamed the computer to PC1.

Under member of select domain.

Enter the domain name and select OK.

image

A prompt will appear to enter administrative privileges to add the computer to the domain.

Enter the administrative credentials and select OK.

image

The computer was added to the domain.

The computer will be restarted.

image

After the restart sign in as a domain user.

image

I am now signed as a domain user.

image

I configured the computer to receive a DHCP address.

image

I confirmed that a DHCP address is in use by the doing the ipconfig /all command in command prompt.

# **Creating Group Policies**

image

Go to the start menu of the domain controller and search for Group Policy Management.

Select Group Policy Management.

image

image

Select the domain and right click>Select “Create a GPO in this domain, and link it here”.

image

Enter the name of the Group Policy Object. 

I am creating a password policy.

Select OK.

image

To configure the policy right click the policy and select edit.

image

To find the appropriate policy settings select computer configuration>policies>windows settings>security settings>account policies>password policy.

image 

image

I configured the policy.

image

I also configured an account lockout policy.

After 4 invalid logon attempts an account will be locked.

image

I placed the PC1 computer in a computers Organizational Unit that I created.

image

I forced the group policies to be implemented on the client computer by inserting the gpupdate /force command in command prompt.

Testing the account lockout policy

Video of me testing the policy.

# **Creating a shared folder**

image

Go to the domain controller and create a folder.

I created a folder in the C: drive.

image

Right click the folder>Select properties

image

Select the sharing tab>Select advanced sharing

image

Select share this folder.

image

Select permissions.

image

This can be left as default.

Select OK.

image

Within the shared folder I created a folder named “Admin Department”

Right click the folder and select properties.

image

Select the sharing tab>Select share.

image

Enter the name of the group to give permission to access the folder.

I entered “Admin Department” and selected add.

image

I gave the group read/write permissions and selected share.

# **Mapping the share drive on the client machine**

image

Go to the client machine and login as a domain user.

Go to “This PC” in the file explorer.

Go to the ribbon at the top and select “Map network drive”.

image

I entered the server name “\\DC1” and selected browse.

image

I selected the share folder and selected OK.

image

Select finish.

image

The drive was successfully mapped.

# **Testing the shared folder permissions**

image

I navigated to the Admin Department folder and attempted to add a text document.

image

The text document was added successfully and this means the read/write configuration worked.

# **Conclusion**
I learned that some policies in GPO can not be implemented at the OU level but has to be linked to the entire domain for example Password policies and account lockout policies are to be attached to the domain.

I plan to expand this home lab and continue to learn more about active directory.