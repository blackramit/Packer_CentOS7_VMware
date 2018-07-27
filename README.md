# Packer_CentOS7_VMware
packer-templates
These are the Packer templates for boxes available at https://vagrantcloud.com/gosddc, they only work with VMware and require the packer-post-processor-vagrant-vmware-ovf post-processor to work.

These templates will output a Vagrant box for each OS version in the new universal format vmware_ovf.

The templates will take care of installing the Operating system from the ISO, install VMware tools, install the Puppet agent and perform a puppet-masterless configuration for Vagrant. It can be easily expanded by adding more puppet modules.
