# apt\_cleanup cookbook

This cookbook vacuum-cleans your apt system.

Service incudes

* Cleaning up apt-cache
* Purging leftovers from removed packages
* Removing old unused kernels (for a cleaner /boot)
* Removes dependencies dragged in by already deleted packages
* Dispenses fresh perfume all over your system

See [this blogpost](http://chr4.org/blog/2013/08/04/apt-get-cleanup-commands/) for more information.

## Supported Platforms

* Ubuntu
* Debian

## Usage

### apt\_cleanup::default

Includes all other cleanup recipes

### apt\_cleanup::remove\_old\_kernels

Removes all old kernels, but the most recent as well as the currenlty used one.

### apt\_cleanup::remove\_unneeded\_packages

Runs `apt-get autoremove` to remove packages not required anymore.

### apt\_cleanup::purge\_removed\_packages

Purges already removed packages, to get rid of e.g. old config files.

### apt\_cleanup::clean\_apt\_cache

Runs `apt-get clean` to remove `.dpkg` files from `/var/cache/apt/archives`.


## Contributing

1. Fork the repository on Github
2. Create a named feature branch (i.e. `add-new-recipe`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request

## License and Authors

Author:: Chris Aumann (<me@chr4.org>)
