pbox
----

Run a gui program inside a fully contained VM

### Features

Runs a contained gui application inside a Linux VM and integrates with your 
desktop.

![pbox](/images/banner.png?raw=true)

Runs on any OS (Windows, OS X, Linux) using multiple hypervisors (VirtualBox, 
VMware, Parallels).

Allows for selective filesystem read/write through folders (for downloading files)
and clipboard integration.

Can easily be reset back to a known state (wipe entire VM) to start fresh

Works with Flash and Java 

### Install

First install
 * [VirtualBox](https://www.virtualbox.org/) or your hypervisor of choice
 * [Vagrant](https://www.vagrantup.com/)

Clone this repository (or download zip and extract)

`git clone https://github.com/rothgar/pbox.git`

run vagrant up to create the VM

`vagrant up`

You may want to [specify `--provider`]
(http://docs.vagrantup.com/v2/getting-started/providers.html) if you would like 
to use something other than VirtualBox (not tested)

*NOTE the first run will take a while (10+ minutes) because packages are 
installed, the system is updated, and the user is configured.*

To switch to seemless mode you can select the view menu -> seemless mode 
(requires virtualbox 5.0.x)

![Seemless](/images/seemless_mode.png?raw=true)

When you are done using pbox you can shut down the VM by going into the folder 
you cloned this repository and running `vagrant halt`

### Refresh VM

Your VM and firefox settings will remain on each boot (using `vagrant up` and
`vagrant halt` but if you want to remove your saved settings and start over you 
should run `vagrant destroy`

### Why would you do this?

Because even if you disable flash and java in your browser you may [not be 
completely secure](https://www.mozilla.org/en-US/security/advisories/mfsa2015-78/)
from people stealing your stuff.

### Acknowledgements

Uses Fedora 22 image provided by [boxcutter](https://github.com/boxcutter/fedora)

### ToDo

 - [ ] Make cli easier (wrapper script)
 - [ ] Make gui launcher better
 - [ ] Put shortcut to shutdown VM
 - [ ] Create smaller base image
 - [ ] Change Firefox homepage
 - [ ] Allow profile syncing from host
 - [ ] Add java support
 - [ ] Investigate smaller base images
 - [ ] Add support for vmware and parallels
 - [ ] Enable audio support
 - [ ] Enable hardware acceleration?
