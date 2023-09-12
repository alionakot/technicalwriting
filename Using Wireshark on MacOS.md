#### Task:  
Create an instruction on filtering the HTTP traffic with Wireshark, including the following:

1. Downloading and installing Wireshark.  
2. Setting up Wireshark to capture traffic from the required interface.  
3. Capturing the HTTP traffic.  
4. Filtering the HTTP traffic.



# Filtering HTTP Traffic with Wireshark on macOS

## What is Wireshark? 
Wireshark is a widely used open-source network protocol analyzer. It allows users to capture and inspect the data traveling back and forth on a computer network. Wireshark is capable of capturing and analyzing data from a variety of sources, including wired and wireless networks, and it provides detailed information about network packets, protocols, and communication flows. It's a valuable tool for network administrators, security professionals, developers, and anyone interested in understanding and troubleshooting network traffic.

This guide will walk you through the process of filtering HTTP traffic using Wireshark on macOS including installing Wireshark itself. By following these steps, you'll be able to capture and analyze HTTP traffic for various purposes, including network troubleshooting and security analysis.

## Downloading and Installing Wireshark
Before we begin, let's start by downloading and installing Wireshark on your macOS computer:
1. Open your preferred web browser.
2. Go to the Wireshark official website at www.wireshark.org.
3. Click on the "Get started" or "Download Wireshark Now" button on the top screen. You'll be transferred to the bottom of the page where you can choose the app version you need.
4. Click on the macOS Arm Disk Image if you have a MacOS with m1/m2 chip or MacOS Intel Disk Image if you have an Intel processor in your Mac. The download will begin automatically.
5. Once the download is complete, open the .dmg file.
6. Drag the Wireshark icon into the Applications folder to install it.

## Setting Up Wireshark for Traffic Capture
Now, let's configure Wireshark to capture traffic from your desired network interface:
1. Launch Wireshark from your Applications folder.  
2. If you see this message (pic. 1), click "installing Chmod BPF". Follow the instructions to install it.  
3. Relaunch Wireshark after installing Chmod BPF.


## Capturing HTTP Traffic
In the main Wireshark window, you'll see a list of available network interfaces.

Select the interface that corresponds to your network connection (e.g., Wi-Fi). 

_Tip: if you're not sure which connection you use, find a chart showing your dynamics of network activity (pic. 2). This is your connection type. Click on the interface twice._

Traffic capturing starts automatically when you select the interface including HTTP traffic.


## Filtering HTTP Traffic
To filter and view only the HTTP-related traffic, use the following steps:
1. In the Wireshark main window, locate the "Display Filter" field at the top.
2. Enter "http" (without quotes) into the filter field and press Enter. This filter will display packets related to HTTP traffic only.

You'll now see a list of packets that match the HTTP filter.

## Conclusion
Congratulations! You've successfully captured and filtered HTTP traffic using Wireshark on your macOS system. By mastering these steps, you can analyze network communications, troubleshoot issues, and enhance your understanding of HTTP traffic patterns. Wireshark offers extensive filtering and analysis options, enabling you to gain valuable insights into network behavior.

Remember to use this knowledge responsibly and in accordance with any legal and ethical considerations, as monitoring network traffic may be subject to legal regulations.
