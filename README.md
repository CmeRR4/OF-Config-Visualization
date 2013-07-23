OF-Config-Visualization
=======================

Visualization of the Management Plane in OpenFlow/SDN Networks


  Project were created on the "Flack" - flash-based map interface for allocating ProtoGENI and 
other supported GENI resources. There were reserved one slice with four nodes. 
Two of them are two LINCs installed on Ubuntu 12.04. The third one is a Network Manager. 
It is hosting the GUI to display all LINC’s OpenFlow parameters. Also, Network Manger runs NETCONF over SSH Client 
that is needed to establish sessions with NETCONF Server on LINCs and retrieve XML configuration schemes. 
NETCONF over SSH Client/Server is a YANG-Based Unified Modular Automation Tool, that is basically plug-in 
to the OpenFlow framework, and it is used to push/pull configurations to /from switches and clients.

  In order to retrieve data there should be connection to the Server ( yangcli> connect server=10.10.11.2 ncport=1830). 
After the session is established configurations from the server can be pulled ( yangcli> @some-name.xml = get-config ) 
and store into some-name.xml file for future manipulations.

  Then XML file is parsing and all the OpenFlow parameters that switches have is displaying in the User Interface.

  Future deployment:
Ability to dynamically change switch configurations directly from the GUI.
