# ZeeQL Installation

TBD

## Install on Linux

Ubuntu packages required (assuming you have Swift 3 installed already):

    sudo apt-get update
    sudo apt-get install libsqlite3-dev

TODO


## APR Driver

### Homebrew

Select the mod_dbd drivers you need:

    brew reinstall apr-util \
		  --with-sqlite \
			--with-mysql \
			--with-postgresql
