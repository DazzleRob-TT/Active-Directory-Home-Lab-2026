# Active Directory Home Lab 2026

## **Introduction**

This is a basic home lab of Active Directory that I attempted using Windows Server 2022.

## What I used to do the lab

#### 1. Virtualization Software: VMware Workstation 25H2

#### 2. Operating systems: Windows Server 2022 and Windows 10


## **Configuring the IP Address of the Server**
![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd60db98b1d0d9f3a17065ecb6fb57c933f6863/Phase%201/IP%20Change1.png)


#### 1. Select Ethernet0 in the Local Sever Tab, IPv4 address assigned by DHCP, IPv6 enabled.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/704d0fe3d5524a10f6adbe961b5c16807e1e30d3/Phase%201/IP%20Change%202.png)


#### 2. Right click Interface select properties.

#### 3. Select Internet Protocol Version 4 (TCP/IPv4) then select properties.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/16ffa733b182ad3097bce2b2629bde3aa5aa7407/Phase%201/IP%20Change%203.png)


#### 4. Select use the following IP address.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/16ffa733b182ad3097bce2b2629bde3aa5aa7407/Phase%201/IP%20Change%204.png)


#### 5. Enter the IP address, subnet mask, and default gateway.

#### 6. At the bottom select use the following DNS server addresses.

#### 7. In the preferred DNS server field enter the DNS server (I used the loopback IP address) and select OK.

# **Changing the computer name**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/3d7e41e023f40a0ff12c923eb9ca446f03d85f0e/Phase%201/Change%20name%201.png)


#### 1. Go to Server Manager then to Local Server. 

#### 2. Select the computer name.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%201/Change%20name%202.png)


#### 3. Select change.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/main/Phase%201/Change%20name%203.png)


#### 4. Enter the computer name (DC1) and select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/3d7e41e023f40a0ff12c923eb9ca446f03d85f0e/Phase%201/Change%20name%204.png)


#### 5. Select OK and restart the virtual machine.

# **Installing roles (AD DS, DHCP, DNS)**

#### 1. Go to Server Manager.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/Adding%20roles%20p1.png)


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%202.png)


#### 2. Select Manage> Add Roles and Features.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%203.png)


#### 3. The Add Roles and Features Wizard will appear.

#### 4. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%204.png)


#### 5. Select Role Based or feature-based installation and select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/a189a5498c461922b034adefab7ece5a0ee1f0c2/Phase%202/Adding%20DC%20Roles/roles%205.png)


#### 6. There is one server, select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%208.png)


#### 7. For the server roles select Active Directory Domain Services, DHCP Server and DNS Server.

#### 8. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%207.png)


#### 9. Select Add Features.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%209.png)


#### 10. In the Features section ensure Group Policy Management is ticked and select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f70c6258649303bcb5cfe4735154ff2623f4066/Phase%202/Adding%20DC%20Roles/roles%2010.png)


#### 11. Select next.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2011.png)


#### 12. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2012.png)


#### 13. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2013.png)


#### 14. Select install.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2014.png)


#### 15. Wait for the installation to complete.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/6fea75f93e407637c6de76c3959710b42c846344/Phase%202/Adding%20DC%20Roles/roles%2015.png)


#### 16. After the installation is completed select promote this server to a domain controller.

# **Server promotion to a Domain Controller**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%202.png)


#### 1. Select add a new forest and enter the root domain name.

#### 2. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%203.png)


#### 3. Select a functional forest and domain level.

#### 4. Enter a Directory Services Restore Mode password.

#### 5. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%204.png)


#### 6. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%205.png)


A NETBIOS name will be generated.

#### 7. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%206.png)


#### 8. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/820af317ebe304f45422c2a9fbfd4fd69910973a/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%207.png)


#### 9. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%202/Promoting%20Server%20to%20DC/Promo%20to%20DC%208.png)


#### 10. Select install.

The server will be restarted and the server will be become a domain controller.

# **Creating users and groups in Active Directory**


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/Users%20and%20groups%201.png)


#### 1. Go to Server Manager then Tools select Active Directory Users and Computers.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%202.png)


#### 2. Select the domain drop down. 

#### 3. In the right pane section right click. 

#### 4. Go to New>Organizational Unit


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%203.png)


#### 5. Enter a name. 

#### 6. Select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%204.png)


#### 7. I made another Organizational Unit within the previous one and named it “Users”.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%205.png)

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/68a2f243aa8e6d45567ebd5cc7bc9df2cb1ad315/Phase%203/Creating%20users%20and%20groups/UG%206.png)


#### 8. Within the Users Organizational Unit I made a Group called Admin Department.

# **Creating a User**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/59ed169539569f2fe5a4c9914cd1588d3927142f/Phase%203/Creating%20users%20and%20groups/UG%207.png)


#### 1. In the right pane section right click. 

#### 2. Go to New>User.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/59ed169539569f2fe5a4c9914cd1588d3927142f/Phase%203/Creating%20users%20and%20groups/UG%208.png)


#### 3. Enter the user credentials.

#### 4. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/59ed169539569f2fe5a4c9914cd1588d3927142f/Phase%203/Creating%20users%20and%20groups/UG%209.png)


#### 5. Create a user password.

For the purposes of this lab I checked the Password never expires box.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/59ed169539569f2fe5a4c9914cd1588d3927142f/Phase%203/Creating%20users%20and%20groups/UG%2010.png) 


#### 6. Select Finished.

The user is now created.

## **Adding a user to a group**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/eae73bcc0ba71f80837fc53b39701e262be3fd3c/Phase%203/Creating%20users%20and%20groups/UG%2012.png)


#### 1. Right click a user.

#### 2. Select add to a group.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/eae73bcc0ba71f80837fc53b39701e262be3fd3c/Phase%203/Creating%20users%20and%20groups/UG%2013.png)


#### 3. Enter the name of the group in the white section.

#### 4. Select check names.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/eae73bcc0ba71f80837fc53b39701e262be3fd3c/Phase%203/Creating%20users%20and%20groups/UG%2014.png)


#### 5. The group was found successfully indicated by the underline.

#### 6. Select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/eae73bcc0ba71f80837fc53b39701e262be3fd3c/Phase%203/Creating%20users%20and%20groups/UG%2015.png)


#### 7. Select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/eae73bcc0ba71f80837fc53b39701e262be3fd3c/Phase%203/Creating%20users%20and%20groups/UG%2016.png)


#### 8. To verify what groups a user is a member of right click the user>then select the member of tab.

# **DHCP Scope Configuration**
## DHCP after the role installation

#### 1. Run the DHCP Post-Install configuration wizard to authorize the DHCP server and press commit. 

#### I Forgot to do this before configuring the DHCP Scope.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/Configuring%20DHCP%201.png)


#### 2. Go to Server manager>Tools>DHCP.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%203.png)


#### 3. Right click IPv4>Select New Scope.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%204.png)


#### 4. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%205.png)


#### 5. Give the scope a name.

#### 6. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%206.png)


#### 7. Enter the IP address range for the scope along the with the length and subnet mask.

#### 8. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%207%20.png)


#### 9. Add any IP address exclusions.

#### 10. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%208.png)


#### 11. Enter the lease duration of an IP address.

#### 12. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%209.png)


#### 13. Select “Yes I want to configure DHCP options now”.

#### 14. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%2010.png)


#### 15. Add an IP address for the default gateway.

#### 16. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%2011.png)

#### 17. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%2012.png)


#### 18. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%2013.png)

#### 19. Select “Yes, I want to activate this scope now”.

#### 20. Select next.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/187cf3bae5f73bb604ee8f8b37268440d1caf442/Phase%204/Configuring%20DHCP/DHCP%2014.png)

#### 21. Select finish.

# **Adding a computer to the domain**

#### 1. Sign into pc.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/ecd2ac444650790a350ee11a4231da53bdbc9674/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/Adding%20PC%20to%20Domain%201.png)


#### 2. Search for and click control panel.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/ecd2ac444650790a350ee11a4231da53bdbc9674/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%202.png)


#### 3. Select network and internet.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/ecd2ac444650790a350ee11a4231da53bdbc9674/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%203.png)


#### 4. Select network and sharing center.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/ecd2ac444650790a350ee11a4231da53bdbc9674/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%204.png)


#### 5. Select change adapter settings.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/ecd2ac444650790a350ee11a4231da53bdbc9674/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%205.png)


#### 6. Right click the adapter>Select properties.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/ecd2ac444650790a350ee11a4231da53bdbc9674/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%206.png)


#### 7. Select Internet Protocol Version 4 (TCP/IPv4).

#### 8. Select properties.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/ecd2ac444650790a350ee11a4231da53bdbc9674/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%207.png)


#### 9. Give the pc an IP address to connect to the domain.

#### 10. Select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%208.png)


#### I opened command prompt and entered the ipconfig /all command to verify the all the IP configuration information.

#### I then tested connectivity with the domain controller by doing a ping command.

#### The test results were successful in that the pc can communicate with the domain controller.

#### 11. The next step is to add the pc to the domain.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%209.png)


#### 12. Right click the start button>Select system.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2010.png)


#### 13. Select advanced system settings.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2011.png)


#### 14. Select change.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2012.png)


#### 15. I renamed the computer to PC1.

#### 16. Under "member of" select domain.

#### 17. Enter the domain name and select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2013.png)


#### 18. A prompt will appear to enter administrative privileges to add the computer to the domain.

#### 19. Enter the administrative credentials and select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2014.png)


#### The computer was added to the domain.

#### The computer will be restarted.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2016.png)


#### After the restart sign in as a domain user.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2017.png)


#### I am now signed as a domain user.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2018.png)


#### I configured the computer to receive a DHCP address.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/4f590230dec2db41e4da865dba863831008de3ec/Phase%205/Adding%20Computer%20to%20Domain%20and%20Signing%20User%20In/ATD%2019.png)


#### I confirmed that a DHCP address is in use by the doing the ipconfig /all command in command prompt.

# **Creating Group Policies**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%201.png)


#### 1. Go to the start menu of the domain controller and search for Group Policy Management.

#### 2. Select Group Policy Management.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%202.png)

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%203.png)


#### 3. Select the domain and right click>Select “Create a GPO in this domain, and link it here”.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%204.png)


#### 4. Enter the name of the Group Policy Object. 

I am creating a password policy.

#### 5. Select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%205.png)


#### 6. To configure the policy right click the policy and select edit.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%206.png)


#### 7. To find the appropriate policy settings select computer configuration>policies>windows settings>security settings>account policies>password policy.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%207.png) 


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%208.png)


#### I configured the policy.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/fbd6c15aa3de6e2cd797cc06c99bca6c26253361/Phase%206/Creating%20GPOs/GPOS%209.png)


#### I also configured an account lockout policy.

#### After four (4) invalid logon attempts an account will be locked.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%206/Testing%20GPOs/GPOS%2010.png)


#### I placed the PC1 computer in a computers Organizational Unit that I created.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%206/Testing%20GPOs/GPOS%2012.png)


#### I forced the group policies to be implemented on the client computer by inserting the gpupdate /force command in command prompt.

## Testing the account lockout policy

### Video of me testing the policy.



https://github.com/user-attachments/assets/96d644bf-8fd2-4769-9404-376efd20e851



# **Creating a shared folder**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sharef1.png)


#### 1. Go to the domain controller and create a folder.

#### 2. I created a folder in the C: drive.

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf2.png)


#### 3. Right click the folder>Select properties


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf3.png)


#### 4. Select the sharing tab>Select advanced sharing


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf4.png)


#### 5. Select share this folder.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf5.png)


#### 6. Select permissions.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf6.png)


#### 7. This can be left as default.

#### 8. Select OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf7.png)


#### Within the shared folder I created a folder named “Admin Department”


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf8.png)


#### 9 .Right click the folder and select properties.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf9.png)


#### 10. Select the sharing tab>Select share.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf10.png)


#### 11. Enter the name of the group to give permission to access the folder.

#### 12. I entered “Admin Department” and selected add.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Adding%20a%20Share%20folder/Sf11.png)


#### 13. I gave the group read/write permissions and selected share.

# **Mapping the share drive on the client machine**

![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/aa0c721efc1ef05e8d1c65dd638a70dfde435138/Phase%207/Mapping%20Share%20Folder/Mapd1.png)


#### 14. Go to the client machine and login as a domain user.

#### 15. Go to “This PC” in the file explorer.

#### 16. Go to the ribbon at the top and select “Map network drive”.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/1de552b928b4cfac436a58b66d07e0a077d5c80e/Phase%207/Mapping%20Share%20Folder/Mapd2.png)


#### 17. I entered the server name “\\DC1” and selected browse.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/1de552b928b4cfac436a58b66d07e0a077d5c80e/Phase%207/Mapping%20Share%20Folder/Mapd3.png)


#### 18. I selected the share folder and selected OK.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/1de552b928b4cfac436a58b66d07e0a077d5c80e/Phase%207/Mapping%20Share%20Folder/Mapd4.png)


#### 19. Select finish.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/1de552b928b4cfac436a58b66d07e0a077d5c80e/Phase%207/Mapping%20Share%20Folder/Mapd5.png)


#### 20. The drive was successfully mapped.

# **Testing the shared folder permissions**


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/1de552b928b4cfac436a58b66d07e0a077d5c80e/Phase%207/Testing%20Share%20Permissions/Testing%20Share%20Permissions%201.png)


#### 1. I navigated to the Admin Department folder and attempted to add a text document.


![alt image](https://github.com/DazzleRob-TT/Active-Directory-Home-Lab-2026/blob/1de552b928b4cfac436a58b66d07e0a077d5c80e/Phase%207/Testing%20Share%20Permissions/TP2.png)


#### 2. The text document was added successfully and this means the read/write configuration worked.

# **Conclusion**
#### I learned that some policies in GPO can not be implemented at the OU level but has to be linked to the entire domain for example password policies and account lockout policies are to be attached to the domain.


#### I plan to expand this home lab and continue to learn more about Active Directory.
