# TelnetApp
Used the TCP/IP Stack to implement LED control and push button monitor on a Mx7CK microcontroller
Note that the TCP/IP Stack was not coded by me and instead was given to me by my professor. 
Modification made on my end was done in ETH795.h file and the creation of LEDTCPServer.c
In order to run the code, the user must first:
  1. Have a MX7cK microcontroller board.
  2. Install the MPLABX software.
  3. Connect the USB cable from the host computer to the Debug USB Port on the board.
  4. Connect Ethernet cable from the host computer to the Ethernet port on the board.
  5. Look for the last 2 digits of the mac address written on the back of the board.
  6. Change some codes in the ETH795.h file
        line 170) #define MY_DEFAULT_MAC_BYTE6 (0xbb) // where bb is the last 2 digits mac address
        line 175) #define MY_DEFAULT_IP_ADDR_BYTE4 (0xbb) // where bb is the last 2 digits mac address
        line 185) #define MY_DEFAULT_GATE_BYTE4 (bbbul) // where bbb is the decimal form of the last 2 digits mac address (in hex)
  6. Build and Run the code.     
  7. Open command console and type the following commands:
        i) Check Ethernet connection using ipconfig and ping 192.168.1.bbb //where bb is the decimal form of the last 2 digits mac                                                                                address (in hex)
        ii) Run telnet interface using "telnet 192.168.1.bbb 7301"/
  8. Type command and corresponding changes will be made to the board.
