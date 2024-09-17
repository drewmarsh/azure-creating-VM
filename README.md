Navigate to the Azure Portal and sign in (create an account and start a subscription if needed).

Click the menu button (**&#8801;**) in the top left to reveal the side panel. Then, click ```Create a resource```.

Under the **Virtual machine** option, click ```Create```.
<br><br>
> [!NOTE]
> The configuration options below should be adjusted accordingly based on use case. For example, for a Windows 10 Pro VM that shuts down automatically and runs osTicket, the following settings would be used.

### Basics Tab
> **Subscription**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select the subscription to be used by the VM.

> **Resource Group**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Click ```Create new``` and enter ```osTicket-RG```, then click ```OK```.

> **Virtual machine name**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter ```osTicket-Win10Pro-VM```.

> **Region*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter preferred region to host the VM.

> **Availability options**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```No infrastructure redundancy required```.

> **Security type**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```Standard```.

> **Image**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search for and select ```Windows 10 Pro, version 22H2 - x64```

> **VM Architecture**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```x64```

> **Size**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```Standard_B2ms - 2 vcpus, 8 GiB memory```

> **Username & Password**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Set up a secure username and password.

### Networking Tab
> **Select inbound ports**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```RDP (3389)```, ```HTTP (80)```, and ```HTTPS (443)```.

### Management Tab
> **Auto-shutdown**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tick the ```Enable auto-shutdown``` checkbox and configure the settings as desired.

<br>
Click the ```Review + Create``` button at the bottom of the page. Verify that validation has passed. Lastly, click ```Create```.

On Windows, simply connect to your newly created VM by using Remote Desktop Protocol (RDP) and entering the public IPv4 address. 

If you are a Mac user then you will have to download Microsoft Remote Desktop. 
