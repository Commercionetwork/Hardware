# How to setup a Validator Node (work in progress)
Guide on how to install a Commercio.network Validator Node.       

## Install OS

## Download Binary here

## Hardware requirements

### Low level (Not Recommended)

This configuration is a basic level with low security level and low high availability configuration.    
It is prone to intrusion and out of service in any moment for breaking hardware or network line problems.    
     
* 1 Server with
  * **Cpu**: Minimun to support last version of most common Operation System
  * **Ram**: 32Gb
  * **Storage**: 1 ssd 1Tb
  * **Power supply**: 1 power supply
  * **Net**: 1 ethernet port with 100 Mbit speed capabilities
* 1 internet Connection with bidirectional capabilities and minimun 30/30Mbit
* 1 Ledger nano S
* 50,000 Commercio Tokens


### Mid level  (Minimum Necessary)

This configuration guarantees a basic security level, the validator node is not directly attached to internet, and basic high availability configuration.    
The redoundant power supply and ethernet nic guarantee a basic 


* 1 Server with
  * **Cpu**: Minimun to support last version of most common Operation System
  * **Ram**: 32Gb
  * **Storage**: 1 ssd 1Tb
  * **Power supply**: 2 power supply to prevent power down if one break
  * **Net**: 2 ethernet port with 100 Mbit speed capabilities
* 1 internet Connection with bidirectional capabilities and minimun 30/30 Mbit
* 1 Firewall with capabilities of vpn site to site connection
* 1 sentry node configured on major service providers (Aws, Azure, Google)
* 1 Ledger nano S
* 1 Ups with 1000VA capacity for minimum resistance to power surges and out of power service 
* 50,000 Commercio Tokens
  


Configurations of nodes:    
**Validator node**
  
| Config        | Setting       |
| ------------- |:-------------:|
| pex      | false |
| persistent_peers     | private sentry node      |
| private_peer_ids | --     |
| addr_book_strict | false     |

**Private sentry node**

| Config        | Setting       |
| ------------- |:-------------:|
| pex      | true |
| persistent_peers     | validator node, own public node     |
| private_peer_ids | validator node id    |
| addr_book_strict | false     |

**Public sentry node**

| Config        | Setting       |
| ------------- |:-------------:|
| pex      | true |
| persistent_peers     | other public sentry nodes    |
| private_peer_ids | validator node id, private node id    |
| addr_book_strict | false     |


### Top Level (Recommended)

* 2 Servers
  * **Cpu**: Minimun to support last server version of most common Operation System
  * **Ram**: 32Gb
  * **Storage**: 2/3 ssd 1Tb with Raid1 or Raid5 configuration
  * **Power supply**: 2 power supply to prevent power down if one break
  * **Net**: 2 ethernet port with 1000 Mbit speed capabilities
* 2 internet Connection with bidirectional capabilities and minimun 100/100 Mbit
* 2 dedicated switch 
* 2 Firewall with capabilities of vpn site to site connection
* 1 Load Balancer AWS
* 2 sentry node configured on major service providers (Aws, Azure, Google)
* 2 Ledger nano S (one per server)
* 50,000 Commercio Tokens

