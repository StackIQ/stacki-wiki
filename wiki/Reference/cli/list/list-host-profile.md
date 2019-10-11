## list host profile

### Usage

`stack list host profile [host] [hash=boolean]`

### Description


	Outputs a XML wrapped installer profile for the given hosts.

	If no hosts are specified the profiles for all hosts are listed.
	
	If input is fed from STDIN via a pipe, the argument list is
	ignored and XML is read from STDIN.  This command is used for
	debugging the Stacki configuration graph.

	

### Arguments

* `{host}`

   Zero, one or more host names. If no host names are supplied, info about
	all the known hosts is listed.


### Parameters
* `{hash=boolean}`

   If 'yes', output a hash for this profile on stderr.
	Default is 'no'.

### Examples

* `stack list host profile backend-0-0`

   Generates a Kickstart profile for backend-0-0.

* `stack list host xml backend-0-0 | stack list host profile`

   Does the same thing as above but reads XML from STDIN.



