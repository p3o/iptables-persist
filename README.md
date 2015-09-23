# Persistent iptables

`iptables-persist` is an `init.d` service that saves automatically `iptable` rules when the system shutdowns and restores them to the saved value after powering up.


## Installation

From a command prompt, run as root (e.g. using `sudo`):
~~~bash
	cp iptables-persist /etc/init.d/
	update-rc.d iptables-persist defaults
	service iptables-persist start
~~~


## Usage

The rules are persisted in `/etc/iptables.persist`

If no persisted rules file exists, `Iptables-persist` uses the currently running `iptables` rules.

To force saving the rules at any other time, run as root:
~~~bash
	service iptables-persist restart
~~~


## License

MIT license. See the LICENSE file for details 

Enjoy!

