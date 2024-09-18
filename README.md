<p align="center">
  <a href="https://github.com/drewmarsh/azure-creating-VM">
    <img src="/images/azure-vm-banner.png" width="700" alt="Banner">
  </a>
</p>
<br>

# 🚀 Getting Started

Navigate to the Azure Portal and sign in (create an account and start a subscription if needed).

Click the menu button (**&#8801;**) in the top left to reveal the side panel. Then, click ```Create a resource```.

<img src="/images/create-a-resource.png" width="358" alt="Create a resource"> <br>

Under the **Virtual machine** option, click ```Create```.

<img src="/images/create-virtual-machine.png" width="498" alt="Create virtual machine"> <br>

# ⚙️ Settings Configuration
> [!NOTE]
> The configuration options below should be adjusted accordingly based on use case. For example, for a Windows 10 Pro VM that shuts down automatically and runs osTicket, the following settings would be used.

### Basics Tab
> **Subscription**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select the subscription to be used by the VM.

> **Resource Group**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Click ```Create new``` and enter ```osTicket-RG```, then click ```OK```.

> **Virtual machine name**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter ```osTicket-VM```.

> **Region**

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

> **Licensing**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tick the &#9989;```I confirm I have an eligible Windows 10/11 license with multi-tenant hosting rights``` checkbox.

<img src="/images/basics-tab.png" width="554" alt="Basics tab"> <br>

### Networking Tab
> **Select inbound ports**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```RDP (3389)```, ```HTTP (80)```, and ```HTTPS (443)```.

<img src="/images/networking-tab.png" width="802" alt="Networking tab"> <br>

### Management Tab
> **Auto-shutdown**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tick the &#9989;```Enable auto-shutdown``` checkbox and configure the settings as desired.

<img src="/images/management-tab.png" width="797" alt="Management tab"> <br>

<br> Click the ```Review + Create``` button at the bottom of the page. Verify that validation has passed. Lastly, click ```Create```.

# 🖥️ Accessing the Virtual Machine Remotely
On the Azure Portal homepage, navigate to the ```Azure services``` section and click ```Virtual machines```. Click on the virtual machine name in question. Then, click the &#9654;```Start``` button on the toolbar.

On Windows, simply connect to your newly created VM by using Remote Desktop Protocol (RDP) and entering the public IPv4 address. 

<img src="/images/run-rdp.png" width="486" alt="Run RDP"> 

<img src="/images/enter-ip.png" width="486" alt="Enter IP"> 

<img src="/images/enter-credentials.png" width="486" alt="Enter credentials"> 

<img src="/images/connect-despite-errors.png" width="486" alt="Connect despite errors">

<img src="/images/connection-successful.jpg" width="486" alt="Connection successful"> <br>

On Mac, downloading [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12) is a prerequisite.

On Linux, downloading Remmina or a similar client is a prerequisite.

# ❌ Deleting the Virtual Machine
Under the ```Virtual machines``` section of Azure, tick the checkbox next to the virtual machine you want to delete. Then, click the &#128465;```Delete``` button in the toolbar in the top right off the webpage.

<img src="/images/delete-vm-1.png" width="1000" alt="Delete VM 1"> <br>

A side panel will open up on the right of the webpage. You must tick the &#9989;```Apply force delete for selected virtual machines and Virtual machine scale sets``` checkbox. Then, type ```delete``` into the text field. Lastly, click the red ```Delete``` button.

<img src="/images/delete-vm-2.png" width="468" alt="Delete VM 2"> <br>
