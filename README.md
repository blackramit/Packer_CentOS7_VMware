# Packer_CentOS7_VMware
This is a Packer template for creation of a CentOS7 VM Image on vSphere 6.5.  The intent is to create an OVF that can be loaded into the vSphere Content Library and utilized by Terraform as described here: https://www.terraform.io/docs/providers/vsphere/r/custom_attribute.html  

This script works with VMware ESXi 6.5 and requires the vmware-ovf post-processor to work.  It will output an .OVF file to a folder in the Project folder on the "Execution Machine".  In my case this is an existing CentOS7 Platform with Packer, Terraform, Git, Ansible and the Vmware OVF Tool installed. 

The templates will take care of installing the Operating system from the ISO and install VMware tools.

My file structure.

.
├── iso
│   ├── CentOS-7-x86_64-Minimal-1804.iso
│   ├── linux.iso
│   ├── VMwareTools-10.1.5-core-5055683.tar.gz
│   └── vmware-tools-linux.iso -> ./linux.iso
├── output-centos7
│   └── centos7
│       ├── centos7-disk1.vmdk
│       ├── centos7.mf
│       └── centos7.ovf
├── packer_cache
├── packer-remote-info.json
├── README.md
├── scripts
│   ├── centos-7-kickstart.cfg
│   ├── centos-vagrant-settings.sh
│   ├── centos-vmware-cleanup_bak.sh
│   ├── centos-vmware-cleanup.sh
│   └── centos-vmware-tools_install.sh
└── templates
    ├── centos7_bak.json
    ├── centos7.json
    └── centos7_working.json
