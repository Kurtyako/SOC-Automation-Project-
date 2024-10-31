# SOC Automation Project

## Objective
 I will be creating a Wazuh instance with SOAR integration along with a case management platform using TheHive


### Skills Learned



### Tools Used



# Part 1 - Network Diagram

This is the network diagram I have put together to clearly represent how the network will flow and how different components interact in this project.

![SOC Diagram](https://github.com/user-attachments/assets/83582fbb-81b0-4106-9706-e92fade58e63)

Here is the diagram without icons and in the style of a flow chart.

![SOC WORD](https://github.com/user-attachments/assets/54cc5d69-dad1-4225-99b0-27bf8d756864)

# Part 2 - Installing Applications on Virtual Machines in Home Lab
## Installing TheHive

I am installing TheHive on a virtual machine I have created that is running Ubuntu 24.04 LTS

1. 11
![hive 1](https://github.com/user-attachments/assets/f09ec46e-4a29-495d-931e-b92c637e3710)

2.  22
![hive 2](https://github.com/user-attachments/assets/e279dbd7-a72c-4d2d-9e13-eb13290cdf5e)

3.  33
![hive 3](https://github.com/user-attachments/assets/1cad4596-52ef-4aba-bc48-adf65557f7b5)

4.  44
![hive 4](https://github.com/user-attachments/assets/c760da8b-9362-4b8e-9428-1033595e4fd4)

5.  55
![hive 5](https://github.com/user-attachments/assets/d2bdca84-7173-4cb3-9d93-480fb60f1f84)

6.  66
![hive 6](https://github.com/user-attachments/assets/b728289a-2943-474c-b993-65aa8db21dab)

7.  77
![hive7](https://github.com/user-attachments/assets/3faeeafd-7660-4301-b955-dcb9548160f6)

8.  88
![hive 8](https://github.com/user-attachments/assets/c2a917c8-7d60-4e47-a9a2-f001dbde9125)

9.  99
![hive 9](https://github.com/user-attachments/assets/01d86c3a-a781-48f5-bb0d-d45650d8e705)

10.  10
![hive 10](https://github.com/user-attachments/assets/0bbc3d63-d5ac-4dbc-80bb-211db7b498b4)

11.  11
![hive 11](https://github.com/user-attachments/assets/31c53f48-4bbc-4baf-88a5-e5c680ce8262)

12.  12
![hive 12](https://github.com/user-attachments/assets/b2ed288a-c733-4cb7-9b17-b042df25d060)

13.  13
![hive 13](https://github.com/user-attachments/assets/d8653e1a-3d99-4e5c-8c0f-54d0b46ae2cd)

14.  14
![hive 14](https://github.com/user-attachments/assets/2da76c75-5208-4bd6-b2ac-08fcf1796840)

15.  15
![hive 15](https://github.com/user-attachments/assets/eb4a1e24-d6e0-46e8-b900-cff139af8b4b)

16.  16
![hive 16](https://github.com/user-attachments/assets/66290d25-2847-4b3d-a44d-b48a3551c89c)

17.  17
![hive 17](https://github.com/user-attachments/assets/54249762-e32c-43ef-8e54-067a4cd52e20)

18.  18
![hive 18](https://github.com/user-attachments/assets/dca8939e-10cd-433d-a316-5de28ba83c52)

19.  19
![hive 19](https://github.com/user-attachments/assets/20448f86-3ed4-4010-933c-1d26be36b8de)

20.  20
![hive 20](https://github.com/user-attachments/assets/83e414f4-edda-4186-9850-ca8043d95f87)

21.  21
![hive 21](https://github.com/user-attachments/assets/5bfa566d-e561-4a74-b2b2-4495cd80dfe8)

22.  22
![hive 22](https://github.com/user-attachments/assets/697f170f-7922-4a43-8433-22d6387c7a2f)

23.  23
![hive 23](https://github.com/user-attachments/assets/d6b7a17a-83dc-47f8-abca-42c3c97749aa)

24.  24
![hive 24](https://github.com/user-attachments/assets/ee512e61-91de-4558-8a4f-df8346d82986)

25.  25
![hive 25](https://github.com/user-attachments/assets/f56a702f-d83d-4b7d-8e00-c6f99b88659c)

## Installing Wazuh

I have already installed Wazuh and have configured it as I have previously completed the Wazuh File Integrity Monitoring and I can repurpose this configuration to fit my needs in this project. These steps and screenshots will be the same as the Wazuh FIM Project

To set up Wazuh, I will be using two virtual machines. One Machine will contain a pre-built virtual machine image in an Open Virtual Appliance(OVA) format containing the following components: Wazuh's manager, indexer, and dashboard. I will use this Wazuh OVA image with Oracle VM Virtual Box. The other virtual machine will be a Windows Server 2022 as my target machine.

1. Starting Windows Server 2022 and Wazuh OVA machine in Virtual Box.   

	![Wazuh virtual box](https://github.com/user-attachments/assets/a1a0d240-cab6-421d-9bad-6ae4ab06e32f)

2. After getting both of the virtual machines up and running my next step is to get the Wazuh agent installed on the Windows 2022 server. From the official Wazuh documentation website, I can download the Wazuh agent and it will look like this when complete:
   
	![download](https://github.com/user-attachments/assets/69024763-cb23-40e9-8020-79f9b57da560)

3. Now I need to get the Wazuh server IP address and the authentication key to link the Wazuh server to the Wazuh Agent.

4. To get the IP address I will run the "ip a" command:
   
	![wazuh ip](https://github.com/user-attachments/assets/bfb8e0f2-4cfb-48e3-8072-76b7cfecc7d9)

5. Next I will get the authenticaion key by accessing /var/ossec/bin/manage_agents on the Wazuh Manager host.
   
	![Wazuh agetn key](https://github.com/user-attachments/assets/c75a97c1-206d-4954-8927-31e465b636f6)

6. Turning back to the Windows Server 2022 we can now import our findings for the IP address and the authentication key.

	 ![Wazuh windows key](https://github.com/user-attachments/assets/4ca85ed1-32bd-41fa-955c-c3db8195b87c)

7. Now to confirm we have set Wazuh up correctly I will try and access the Wazuh dashboard using the IP address of the Wazuh host which is 192.168.100.131 in Firefox.

	 ![wazuh dashboard](https://github.com/user-attachments/assets/be0a8705-c5b6-44d0-b66e-b4fbd51e2c77)

8. After I signed in I can see that the agent is active.

	![Wazuh agent](https://github.com/user-attachments/assets/bb8cbb5c-0135-4796-bfcc-0d6340f51ea7)
























