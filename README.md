# Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/eafc0d88-04d2-45ed-9a1a-828545d2b543"/>
</p>
<p>
First go to Microsoft Azure and type Resource Groups in the search bar
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/180c4847-c7ac-444f-bf10-9c196cd39753"/>
</p>
<p>
Next for the Resource Group name type RG-LAB-02 and the region under US West US 3
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/c1886bb1-df0e-493b-bf4d-f47648bc9d46"/>
</p>
<p>
Then go to the Review and Create section and let the validation passed
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/328ef8c6-1791-4584-9adf-fbd2ddc9bc0d"/>
</p>
<p>
Now go back to Resource Groups and you will see it was created
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/55047fc7-28b7-4b98-810f-c9ffb7d900d5"/>
</p>
<p>
Type Virtual Machines in the search bar
</p>
<br />


<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/56ba9d47-8215-4b55-acf5-a26652e0a2e0"/>
</p>
<p>
Now for the Resource Group click the one we created RG-LAB-02.
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/b0865c84-9f51-426e-8268-41d286ad044c"/>
</p>
<p>
Next type the VM name VM1, and the region under US West US 3, the Image under Windows 10 Pro, and the size under Standard E2s
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/a497a209-c4ac-47cc-931f-26d04bfd2878"/>
</p>
<p>
Next the username will be named labuser and the password can be your own unique password. The Licensing check the box
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/90988751-5779-473b-b8de-84b02d40dc9e"/>
</p>
<p>
Now go to the Networking tab and make sure the Virtual Network, Subnet, and Public IP all says (new)
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/23d49724-a9eb-4114-87b9-91b812ac7185"/>
</p>
<p>
Now go to the Review and create tab and click the Create tab on the bottom left
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/706080ec-1b1b-4aea-a837-580bc1f7051a"/>
</p>
<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/710a84ef-0239-48a0-9eff-4d05861e0694"/>
</p>
<p>
Next let the deployment process load, once its done a green check will emerge near the deployment
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/087b7069-7434-4169-86a3-243c5052aa19"/>
</p>
<p>
Next go type Virtual Machine and click VM1
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/5f905f73-3bea-44d9-8c69-1fc3d5f04717"/>
</p>
<p>
Now click create Azure Virtual Machine 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/34471641-08dc-46f6-b7d9-e375507826c8"/>
</p>
<p>
Next click the Resource group name under RG-LAB-02, the Vritual Machine Name under VM2 and the region US WEST US 3
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/12b7e3ea-d98a-499d-9120-c684fa83b381"/>
</p>
<p>
Now for the Image put Ubuntu Sever Gen2 and the size under Standard E2
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/5cec14e8-6b7a-4bf2-b38e-7a086dc5304a"/>
</p>
<p>
Next for the authentication type click password, under Username type labuser and the password tpye the password
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/d9cc47ae-10b4-4151-9802-f064dec766f0"/>
</p>
<p>
Now go to the networking tab and make sure virtual network, subent, and public IP all says (new)
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/3317e873-cb0f-4811-bc68-d45161b14ddf"/>
</p>
<p>
Next go to the Review and create tab and click create at the bottom left
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/ac445adc-0b2b-4afd-a80f-4cac79202329"/>
</p>
<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/d6588b6f-e9e9-4eb3-9625-5288dd80bdc9"/>
</p>
<p>
Now the deployment process will begin. Then once it's done a green check will appear
</p>
<br />


<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/985f1bc1-e23e-4f69-934f-39e3191f736d"/>
</p>
<p>
Next you can upload all the info in a notepad file
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/7c7c1e49-e7e2-49f4-bd0f-7719c4fe55bc"/>
</p>
<p>
Next type Virtual Machine in the search bar
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/3f609f82-1e60-4995-a335-68817e960034"/>
</p>
<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/b01814be-7d8e-46ac-b115-64ee446e7a7b"/>
</p>
<p>
Next you will see the VM has been created click VM1 and copy the public IP address 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/1c1882df-c967-4a17-9c3c-e17a758326ee"/>
</p>
<p>
Next type Remote Desktop Connection in the search bar
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/4492891b-4d35-438e-841f-7ebfc8d61e3f"/>
</p>
<p>
Next type the public IP of VM1 in the computer seciton and click the connect buttton
</p>
<br />


<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/cf6e558f-9dce-435f-81ed-da213b8aa962"/>
</p>
<p>
Next type the username as labsuer and the password as the password you created, then click the blue ok button
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/e9bf21e7-673e-4d12-85f8-6c962879de4c"/>
</p>
<p>
Then click the yes button 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/aeeeb482-ae64-41f3-84b8-2ba09c6197f7"/>
</p>
<p>
Then click no for all of the following in the image above
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/53dfbcf4-7bec-4265-b871-5f40ff4bfacb"/>
</p>
<p>
Then once the networking tab loads click the yes button 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/635e5b7f-36f7-445c-b242-3dd7657d5e22"/>
</p>
<p>
Next load Microsoft Excel and click start without yuor data 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/0b3954de-a815-4925-ab20-281f00b6bdd6"/>
</p>
<p>
Next click continue without this data
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/7d3ef272-5a59-4762-b478-82853a259fde"/>
</p>
<p>
Now click confirm and continue 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/9ede1e3a-0f9e-41ad-9055-dc84881b77d6"/>
</p>
<p>
Next click confirm and start browsing
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/cc24e06b-d005-44bd-875b-1df9e5ae99eb"/>
</p>
<p>
Now type download wireshark in the search bar 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/68b0f045-3074-4433-9c09-985104a61ced"/>
</p>
<p>
Now click go to download 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/da49f9cc-3ef1-435d-bac2-b1f6805ff647"/>
</p>
<p>
Now click windows x64 installer 
</p>
<br />

<p>
<img src="https://github.com/Jacobvillagomez1/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/assets/143027686/1950ba4a-ce67-4179-896f-71dba49088d5"/>
</p>
<p>
Once the process is done click the file to open in or go to file explorer and open the file in the downloads folder
</p>
<br />
