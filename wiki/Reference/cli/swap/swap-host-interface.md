## swap host interface

### Usage

`stack swap host interface {host ...} {interfaces=string} [sync-config=boolean]`

### Description


	Swaps two host interfaces in the database.

	

### Arguments

* `[host]`

   Host name of machine


### Parameters
* `[interfaces=string]`
* `{sync-config=boolean}`

   If "yes", then run 'stack sync host config' and 'stack sync host network'
	at the end of the command. The default is: yes.


