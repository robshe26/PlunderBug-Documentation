# Plunder Bug - Initial Use Instructions

This is the documentation for the use of the `Plunder Bug` device 

## Initial Setup 

1. Connect the Plunder Bug into a computer running a network analyzer such as Wireshark.
   - The light on the tool will turn green to indicate that it is powered

2. Look for a new network interface titled `ASIX AX88772C USB Ethernet`

3. Using two Ethernet cables, plug the Plunder Bug inline between any two devices.
   - The packets between the two ports will be mirrored on the USB-C tap port.
      - These may be viwed using common open source packet analyzers. 
