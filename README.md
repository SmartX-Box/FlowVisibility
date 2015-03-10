# README #

FlowVisibility : Java based Visibility (Monitoring) in the Flow/Packet Level

## Summary ##

### Overview ###
This tool is developed for configuring and monitoring OpenFlow based network by utilizing tapping mechanism through OpenFlow Controller (OpenDayLight). 

### Release Version ###
This is the first version of the tools. Next Release (Works) will be Distributed FlowVisibility Tool include setup visualization.

## How it works ##

### Network (Physical) Setup ###
In order to run this tool, the required network setup is:
![FlowTapping.jpg](https://bitbucket.org/repo/bjAzAx/images/1737790542-FlowTapping.jpg)
### Required Components ###
Then also some required components such as:

* Switch (Hardware or Software) supporting Traffic SPAN/Mirroring
* OpenDayLight (OpenFlow) Controller - [www.opendaylight.org](www.opendaylight.org)
* Laptop/PC with two interfaces (configuration and capture)
* Eclipse for building and debugging the codes - [www.eclipse.org](www.eclipse.org)

### Current Features ###
The current features include:

* Flow Tapping Configuration based on OpenDayLight REST API - [https://wiki.opendaylight.org/view/OpenDaylight_Controller:REST_Reference_and_Authentication](https://wiki.opendaylight.org/view/OpenDaylight_Controller:REST_Reference_and_Authentication)
* Flow Summary (Basic Processing) based on JNetPcap Library - [http://jnetpcap.com/](http://jnetpcap.com/)
* Flow Visualization based on NetGrok project - [http://www.cs.umd.edu/projects/netgrok/](http://www.cs.umd.edu/projects/netgrok/)
* Flow Inspection based on JEthereal project - [http://yuba.stanford.edu/JEthereal/](http://yuba.stanford.edu/JEthereal/)

## How to Build and Run ##

### Dependencies ###

* Java Version - [Oracle Java](https://java.com/en/download/manual.jsp)
* Pcap Library (Linux/Windows) - [LibPcap](http://www.tcpdump.org/#latest-release) or [WinPcap](https://www.winpcap.org/install/)
* JNetPcap Library - JNetPcap Library - [http://jnetpcap.com/](http://jnetpcap.com/)

### How to Build and Run ###

Downloading the source code manually from:
**https://ariscahyadi@bitbucket.org/ariscahyadi/flowvisibility.git**

Import the source code into Eclipse Project
See this link for details [Importing Existing Project](http://help.eclipse.org/juno/index.jsp?topic=%2Forg.eclipse.platform.doc.user%2Ftasks%2Ftasks-importproject.htm)

Import directly from Git directory
See this link for details [EGit/User Guide](http://wiki.eclipse.org/EGit/User_Guide)

Build and Run the Code
Click **Project** and **Run** from the Eclipse Menu

### Main Windows (GUI) ###

Successful running will be shown this main GUI.

## How to Use (Guidelines)  ##

### SPAN/Mirroring Verification ###
Depends on your switch that you are using, check the mirroring status.
For OpenFlow based software switch (Open vSwitch) use this command:

### Tapping Configuration ###

* Open the OpenFlow controller for the tapping switch and check the ports number/name.
* Open the Tapping configuration in the Flow visibility Tools (Configuration > Tapping Configuration)
* Enter the required information (Controller information, Flow Match/Filter, and Port Destination)
* Apply the Tapping Policy or Configuration

### Starting Flow Capture ###
* Start the Flow Capture (Control > Start Capture)

### Checking Update Main GUI ###
Check the main GUI will be updated automatically.

### Flow Details : Inspection and Visualization ###
* Flow Inspection based on JEthereal project will open the captured file (Flow Details > Flow Inspection)
* Flow Visualization based on NetGrok Project will visualize the information stored in the Pcap file (Flow Details > Flow Visualization)

## Support and Contribution ##

* Author : Aris Cahyadi Risdianto
* Contact : aris.risdianto@gmail.com or TEIN-GIST@nm.gist.ac.kr