---
page_type: sample
languages:
- java
products:
- azure
extensions:
- services: network-watcher,virtual-network
- platforms: java
---

# Getting Started with Network - Verify Network Peering With Network Watcher - in Java #


  Azure Network sample for verifying connectivity between two peered virtual networks using Azure Network Watcher.
 
  Summary ...
 
  - This sample uses Azure Network Watcher's connectivity check to verify connectivity between
    two peered virtual networks.
 
  Details ...
 
  1. Define two virtual networks network "A" and network "B" with one subnet each
 
  2. Create two virtual machines, each within a separate network
    - The virtual machines currently must use a special extension to support Network Watcher

  3. Peer the networks...
    - the peering will initially have default settings:
    - each network's IP address spaces will be accessible from the other network
    - no traffic forwarding will be enabled between the networks
    - no gateway transit between one network and the other will be enabled
 
  4. Use Network Watcher to check connectivity between the virtual machines in different peering scenarios:
    - both virtual machines accessible to each other (bi-directional)
    - virtual machine A accessible to virtual machine B, but not the other way
 
 

## Running this Sample ##

To run this sample:

Set the environment variable `AZURE_AUTH_LOCATION` with the full path for an auth file. See [how to create an auth file](https://github.com/Azure/azure-libraries-for-java/blob/master/AUTH.md).

    git clone https://github.com/Azure-Samples/network-java-use-network-watcher-to-check-connectivity.git

    cd network-java-use-network-watcher-to-check-connectivity

    mvn clean compile exec:java

## More information ##

[http://azure.com/java](http://azure.com/java)

If you don't have a Microsoft Azure subscription you can get a FREE trial account [here](http://go.microsoft.com/fwlink/?LinkId=330212)

---

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.