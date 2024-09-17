- Navigate to the Azure Portal and sign in (create an account and start a subscription if needed).
- Click the menu button in the top left to reveal the side panel. Then, click ```Create a resource```.
- Under the **Virtual machine** option, click ```Create```.

> [!NOTE]
> The rest of  the configuration options should be adjusted accordingly based on use case. For example, for a Windows 10 Pro VM that shuts down automatically and runs osTicket, the following settings would be used.

### Basics Tab
> **Subscription**

Select the subscription to be used by the VM.

> **Resource Group**

Click ```Create new``` and enter ```osTicket-RG```, then click ```OK```.

> **Virtual machine name**

Enter ```osTicket-Win10Pro-VM```.

> **Region*

Enter preferred region to host the VM.

> **Availability options**

Select "No infrastructure redundancy required".

> **Security type**

Select "Standard".


- Image: Search for and select "Windows 10 Pro, version 22H2 - x64"
- VM Architecture: "x64"
- Size: "Standard_B2ms - 2 vcpus, 8 GiB memory"
- Set up a secure username and password.

### Networking Tab
- Under "Select inbound ports", select RDP (3389), HTTP (80), and HTTPS (443).

### Management Tab
- Configure auto shutdown

Click the 'Review + Create' button at the botom of the page. Verifiy that validation has passed. Lastly, click 'Create'.

On Windows, simply connect to your newly created VM by using Remote Desktop Protocol (RDP) and entering the public IPv4 address. If you are a Mac user then you will have to download Microsoft Remote Desktop. 
