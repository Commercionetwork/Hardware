# How to setup a Commercio.network validator node 

See the [official Commercio.network documentation](https://docs.commercio.network/nodes/hardware-requirements.html) for details 
and updated info.

## Hardware Requirements

### Low level (Not Recommended)
This configuration is a basic level with low security level and low high availability configuration.    
It is prone to intrusion and out of service in any moment due to hardware failure or network line problems.    
     
* 1 Server with
  * **CPU**: Bare minimum to support the last version of most common operative systems
  * **Ram**: 32GB
  * **Storage**: 1 x 1TB SSD
  * **Power supply**: 1 power supply
  * **Network**: 1 ethernet port with 100 Mbit speed capability
* 1 internet connection with 30/30Mbit bidirectional capability
* 1 [Yubi HSM2](https://www.yubico.com/product/yubihsm-2/)
* 50,000 Commercio Tokens


### Mid level  (Minimum Necessary)
This configuration guarantees a basic security level due to the fact that the validator node is not directly 
attached to the internet. It also guarantees a fair availability due to the double power supply and ethernet connection. 

* 1 Server with
  * **CPU**: Bare minimum to support the last version of most common operative systems
  * **Ram**: 32GB
  * **Storage**: 1 x 1TB SSD
  * **Power supply**: 2 x power supplies (to prevent power down if one breaks)
  * **Net**: 2 x Ethernet port with 100 Mbit speed capabilities
* 1 internet connection with 30/30Mbit bidirectional capability
* 1 firewall with an on-site VPN capability
* 1 sentry node configured on a major service provider (AWS, Azure, Google)
* 1 [Yubi HSM2](https://www.yubico.com/product/yubihsm-2/)
* 1 UPS with 1000VA capacity for minimum resistance to power surges and out of power services
* 50,000 Commercio Tokens
 

### Top Level (Recommended)
This configuration ensures high availability and keeps the chances of getting slashed at the minimum possible. It works
with two different server to ensure that even if one fails completely the other one can kick in and replace it until 
the first is properly fixed.

* 2 Servers
  * **CPU**: Bare minimum to support the last version of most common operative systems
  * **Ram**: 32GB
  * **Storage**: 2/3 x 1TB SSD with RAID 1 or RAID 5 configuration 
  * **Power supply**: 2 x power supply (to prevent power down if one breaks)
  * **Net**: 2 x ethernet port with 1000 Mbit speed capabilities
* 2 internet connections with 100/100Mbit bidirectional capability
* 2 dedicated switches
* 2 firewalls with an on-site VPN capability
* 1 AWS Load Balancer
* 2 sentry node configured on major service providers (AWS, Azure, Google)
* 2 [Yubi HSM2](https://www.yubico.com/product/yubihsm-2/) (one per server)
* 50,000 Commercio Tokens


