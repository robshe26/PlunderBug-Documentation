# Plunder Bug - Initial Use Instructions

This is the documentation for the use of the `Plunder Bug` device 

## Initial Setup 

1. Connect the Plunder Bug into a computer running a network analyzer such as Wireshark.
   - The light on the tool will turn green to indicate that it is powered

2. Look for a new network interface titled `ASIX AX88772C USB Ethernet` in `ncpa.cpl`

___It should appear similar to this:___
<img width="2248" height="1184" alt="image" src="https://github.com/user-attachments/assets/96ff6ba9-2f35-4d52-a340-cc8ded1e75ce" />


3. Using two Ethernet cables, plug the Plunder Bug inline between any two devices.
   - The packets between the two ports will be mirrored on the USB-C tap port, in my case listed as Ethernet 6.
      - These may be viwed using common open source packet analyzers.

___This is an example packet capture between two PCs pinging each other:___
<img width="2877" height="1702" alt="Screenshot 2026-04-15 211007" src="https://github.com/user-attachments/assets/6cc6536b-80aa-4626-8b28-cf8e8296e67a" />

___
### If the Plunder Bug does not show up in Wireshark

If this is the case there are steps to take to make it visible 

1. Make sure you are running WireShark as Administrator
2. Make sure that Npcap is installed with Wireshark with the "Install Npcap in WinPcap API-compatible Mode" box checked
3. In Wireshark, click capture thne select refresh interfaces
___
## Mode Switching

The Plunder Bug can be used in a bidirectional manner, meaning that in addtion to recieveing a mirror of the traffic, it can aslo act as an addtional Ethernet Port on the target LAN. 

### Operating System Specifc

To switch between passive(muted) and active(unmutted), the Plunder Bug mute script must be completed specific to your machine. 

#### Windows Mode Switching

##### Powershell

1. Download the plunderbug.ps1 Powershell script for Windows platforms from [Hak5 Download Center](https://downloads.hak5.org/bug)

2. Open Powershell using `powershell -exec bypass` with Windows + R

3. Change to the directory of the downloaded script and executre with the numte or unmute parameter (ex: `.\plunderbug.ps1 mute`)
   - Click through the following promts 
   - This setting will stay in effect until the script is run again with the opposite direction

##### Manually 

1. Go to `ncpa.cpl` via Windows + R
2. Click Plunder Bug interface and then select Properties
3. Uncheck the boxes next to each of the protocols 

