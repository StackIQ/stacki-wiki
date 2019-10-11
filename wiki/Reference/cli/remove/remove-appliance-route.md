## remove appliance route

### Usage

`stack remove appliance route {appliance ...} {address=string}`

### Description


	Remove a static route for an appliance type.

	

### Arguments

* `[appliance]`

   Appliance name. This argument is required.


### Parameters
* `[address=string]`

   The address of the static route to remove.

### Examples

* `stack remove appliance route backend address=1.2.3.4`

   Remove the static route for the 'backend' appliance that has the
	network address '1.2.3.4'.



