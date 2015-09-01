## remove host route

### Usage

`stack remove host route {host} {address} [address=string]`

### Description

Remove a static route for a host.

### Arguments

* `{host}`

   Name of a host machine. This argument is required.

* `{address}`

   The address of the static route to remove. This argument is required.


### Parameters
* `[address=string]`

   Can be used in place of the 'address' argument.

### Examples

* `stack remove host route compute-0-0 1.2.3.4`

   Remove the static route for the host 'compute-0-0' that has the
	network address '1.2.3.4'.


