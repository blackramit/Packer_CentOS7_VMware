# Packer_CentOS7_VMware
This is a Packer template for creation of a CentOS7 VM Image on vSphere 6.5.  The intent is to create an OVF that can be loaded into the vSphere Content Library and utilized by Terraform as described here: https://www.terraform.io/docs/providers/vsphere/r/custom_attribute.html  

This script works with VMware ESXi 6.5 and requires the vmware-ovf post-processor to work.  It will output an .OVF file to a folder in the Project folder on the "Execution Machine".  In my case this is an existing CentOS7 Platform with Packer, Terraform, Git, Ansible and the Vmware OVF Tool installed. 

The templates will take care of installing the Operating system from the ISO and install VMware tools....
