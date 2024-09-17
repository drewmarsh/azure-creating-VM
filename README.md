- Navigate to the Azure Portal:
Go to portal.azure.com and sign in.
- Click the hamburger button in the top left to reveal the side panel menu. Then, click 'Create a resource'.
- Under the "Virtual machine" option, click 'Create'.

The rest of  the configuration options should be adjusted accoringly based on use case. For example, for implementing osTicket in a Windows 10 VM on Azure that shutsdown automatically, the following settings would be used:

### Basics Tab
- Select the Subscription to be used by the VM.
- Under "Resource Group", click 'Create new' and enter "osTicket-RG", then click 'OK'.
- Under "Virtual machine name", enter "osTicket-Win10Pro-VM".
- Enter preferred region to host the VM.
- Availability options: Select "No infrastructure redundancy required"
- Security type: "Standard"
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