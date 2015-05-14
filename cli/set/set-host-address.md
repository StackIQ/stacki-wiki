## set host address

### Usage

`stack set host address {host} [dns=string] [domain=string] [gateway=string] [ip=string] [netmask=string] [shortname=string]`

### Description

Change the networking info for a frontend.

### Arguments

* `{host}`

   The name of the frontend.


### Parameters
* `[dns=string]`

   The new public DNS. For example, '8.8.8.8'.
* `[domain=string]`

   The new domain name. This is the last part of the FQDN. For
	example, if the FQDN is a.yoda.com, then the domain name is
	'yoda.com'.
* `[gateway=string]`

   The new public gateway.
* `[ip=string]`

   The new IP address.
* `[netmask=string]`

   The new netmask (e.g., 255.255.0.0).
* `[shortname=string]`

   The new short name. This is the first part of the FQDN. For
	example, if the FQDN is a.yoda.com, then the short name is 'a'.

### Examples

* `stack set host address localhost ip=1.2.3.4`

   Change the frontend's IP address to 1.2.3.4.


