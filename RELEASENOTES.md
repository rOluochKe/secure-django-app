Coffeeshop Application a Secure Web Application Development


### Vagrant issue with IP address outside allowed range

Since the app's writing, Virtualbox no longer allows the IP addresses our VMs run on by default.  This issue affects Linux and Macs with Intel hardware.  If you see this error message:

```
The IP address configured for the host-only network is not within the
allowed ranges. Please update the address used to be within the allowed
ranges and run the command again.

  Address: 10.50.0.2
  Ranges: 192.168.56.0/21

Valid ranges can be modified in the /etc/vbox/networks.conf file. For
more information including valid format see:

  https://www.virtualbox.org/manual/ch06.html#network_hostonly
```

then create a file called `/etc/vbox/networks.conf`, eg with

```
sudo mkdir /etc/vbox/
sudo nano /etc/vbox/networks.conf
```

with the following two lines:

```
* 10.0.0.0/8 192.168.0.0/16
* 2001::/64
```

### Firefox Total Cookie Protection

The exercises on CSRF attacks no longer work as described in Firefox.  This is because of a new Firefox feature, *Total Cookie Protection*.

You have three options:

1. Skip the exercise **Launching a CSRF Attack** fron *Hiding the Response* onwards.
2. Do the exercise in Chrome, with HTTPS.  See the description under **CSRF Attacke** in Section 8.2 for instructions
3. Turn off Total Cookie Protection in Firefox: In Firefox, go to *Settings*, select *Privacy & Security*.  Under *Enhanced Tracking Protection*, click on *Custom* and uncheck *Cookies*.

Version History
---------------
The latest version is 1.0.
