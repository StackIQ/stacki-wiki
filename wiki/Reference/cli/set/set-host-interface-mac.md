## set host interface mac

### Usage

`stack set host interface mac {host} {mac=string} [interface=string] [network=string]`

### Description


	Sets the mac address for named interface on host.

	

### Arguments

* `[host]`

   A single host.


### Parameters
* `[mac=string]`
* `{interface=string}`
* `{network=string}`

   Network name of the interface.

### Examples

* `stack set host interface mac backend-0-0 interface=eth1 mac=00:0e:0c:a7:5d:ff`

   Sets the MAC Address for the eth1 device on host backend-0-0.



