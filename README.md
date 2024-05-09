# smartAgricultre
Repository containing code and documentation for a smart agriculture tool. Utilizes wireless communication modules to monitor soil moisture levels and automate watering. Includes Arduino sketches, Python scripts, and system documentation.

1. Boot up 2 arduino/Receiver Xbee and connect it to a computer with Arduino IDE
2. Connect a cordinator Xbee to a computer with XCTU, but we connect this one to be able to connect to two arduinos.
3.  make sure that you set up the coordinator in broadcast mode (DH= 0x0, DL= 0xFFFF) and all the Xbee devices are in the same network (e.g., ID = 1111).
4. To the first arduino, add the passover code.
5. Now connect the arduinos to the computer with the XCTU,
6. Make sure the two Xbees have compatible device roles, network IDs and destination addresses. Ensure the API mode is set to the Transparent Mode [0] 
   Just remember that we are now connecting two arduinos to the raspberry Pi, like in Lab 5. 
    
7. Make sure the 3 machines are paired
8. Disconnect the Arduino from the PC
9. Connect the arduino1 to the Sensor with the following diagram, but do not power on, you nmeed to confirm with the teacher if this is safe, 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/95a1b2b0-caa2-4e25-a44d-df06a0ea8902/5b9b1420-49d0-4244-ba73-01fae5ae4efa/Untitled.png)

10. Once the machine is safe to turned on, connect the arduiono to the computer with the IDE
11. Upload the Transmitting code
12. Observe the results in the XCTU with the coordinator, you should be receiving the moisture.
13. information from the Sensor every 2 seconds. If you are not receiving anything in XCTU, doublecheck that the coordinator and router can talk to each other.
14. Now that you confirm the messages come through, get rid of `XBee.print("Moisture Sensor Value:");`
15. With the Second Arduino, add the Blink code.
16. And wire it up in the following config
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/95a1b2b0-caa2-4e25-a44d-df06a0ea8902/179c6ad1-e38f-4b99-8f28-4f9e64a18995/Untitled.png)
    
17. Now fire up the raspbberry pi
18. Plug in your USB keyboard and Mouse into the USB slots on the Raspberry Pi.
19. Connect the raspberry pi to the monitor, and disconnect the display cable that is already pluged in. If it fails, unplug everything and replug, that includes 
    power and display
20. Log in with: Username “pi” with the Password “raspberry”
21. Disconnect the Cordinator Xbee from the PC, and plug it into the Raspberry PI
22. On the raspberry Pi, open terminal: run the command: `pip3 install pyserial` It might already be installed, then no worrie
23. Open the Thonny python IDE, and copy the Python-RaspPi code
24.  The HTML file is the dashboard to transmit all the data. download it, and run it, If we had to tweak the `Config` part. then edit the html file and also adjust the top config part.
