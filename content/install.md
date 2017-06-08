# ZeeQL Installation

> WORK IN PROGRESS, STAY TUNED

## Install on Linux

Ubuntu packages required (assuming you have Swift 3 installed already):

    sudo apt-get update
    sudo apt-get install libsqlite3-dev

To compile the standalone PostgreSQL driver:

    sudo apt-get install libpq-dev
    
When using mod_dbd, mod_dbd drivers can be installed as desired:

    sudo apt-get install \
      libaprutil1-dbd-sqlite3 \
      libaprutil1-dbd-pgsql

> WORK IN PROGRESS, STAY TUNED


## APR Driver

### Homebrew

Select the mod_dbd drivers you need:

    brew reinstall apr-util \
		  --with-sqlite \
			--with-mysql \
			--with-postgresql

> WORK IN PROGRESS, STAY TUNED
