pbox
----

Run a gui program inside a fully contained VM

### Features

Runs a contained gui application inside a Linux VM and integrates with your desktop.

Runs on any OS (Windows, OS X, Linux) using multiple hypervisors (VirtualBox, VMware, Parallels).

Allows for selective filesystem read/write through folders (for downloading files)
and clipboard integration.

Can easily be reset back to a known state (wipe entire VM) to start fresh

Works with Flash and Java if needed (flash is installed by default)

### Install

Dependancies

[VirtualBox](https://www.virtualbox.org/) or your hypervisor of choice
[Vagrant](https://www.vagrantup.com/)

Clone this repository (or download zip and extract)

`git clone https://github.com/rothgar/pbox.git`

run vagrant up to create the VM

`vagrant up`

You may want to specify `--provider` if you would like to use something other than VirtualBox

*NOTE* the first run will take a while because packages are installed, the system is updated, and the user is configured.

### Why would you do this?

Because even if you disable flash and java in your browser you may [not be completely secure](https://www.mozilla.org/en-US/security/advisories/mfsa2015-78/) from people stealing your stuff.

### Acknowledgements

Uses Fedora 22 image provided by [boxcutter](https://github.com/boxcutter/fedora)
