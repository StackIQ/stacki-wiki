Adding a pallet expands the range of software available to backend machines. Newer versions of the OS (6.6 vs. 6.5), different distributions (e.g. RedHat instead of CentOS), updated OS packages, application packages with a yum repository etc. can all be added as a pallet. Once a pallet is added and enabled, a backend machine can have the desired RPMS installed with either yum or install/reinstall of the machine. 

### Adding a pallet - simple case:

Let's presume we have a stacki frontend with just two pallets, "stacki" and CentOS v6.5. The stacki pallet and an OS pallet are the minimal pallets that will make up any given distribution. (See "Adding Distributions" in the sidebar for further discussion of distributions.)

% List the pallets you currently have:

    stack list pallet

![test](../images/stack-list-pallet-1.png)

% Download the CentOS 6.6 DVD 1 ISO to the stack frontend. (This may take a bit....)

`# cd /export`  
`# wget http://mirror.umd.edu/centos/6.6/isos/x86_64/CentOS-6.6-x86_64-bin-DVD1.iso`

(You can also torrent this. If you want to add the DVD2 iso, download that too and do the following steps for that ISO as well, and you should probably check the MD5 sums after download.)

% Add the pallet

`# stack add pallet CentOS-6.6-x86_64-bin-DVD1.iso`

Like this:

![stack add pallet](../images/stack-add-pallet-1.png)

% Enable new pallet, disable old pallet.

You don't want two OS pallets of different version being installed. So disable the old CentOS pallet, and enable the new one. (The version is listed in the output of `# stack list pallet`.)

Disable:  
`# stack disable pallet CentOS version=6.5`

Enable:  
`# stack disable pallet CentOS version=6.6`





