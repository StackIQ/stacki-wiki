## load storage controller

### Usage

`stack load storage controller {file=string} [processor=string]`

### Description


	Take rows from a spreadsheet that describe how a host's disk controller
	should be configured and then place those values into the database.

	

### Parameters
* `[file=string]`
* `{processor=string}`

   The processor used to parse the file.
	Default: default.

### Examples

* `stack load storage controller file=controller.csv`

   Read disk controller configuration from controller.csv and use the
	default processor to parse the data.



