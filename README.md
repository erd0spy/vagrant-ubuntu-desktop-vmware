# **Vagrant Ubuntu Desktop VMware**

## **Purpose**

Managing VMware Ubuntu Desktop virtual machine with vagrant.

## **Requirements**

### **Software**

- Vagrant
- VMware

### **Vagrant requirements**

#### `vagrant-vmware-desktop` plugin

```bash
vagrant plugin install vagrant-vmware-desktop
```

#### `Vagrant vmware` Utility

- Download Link: https://www.vagrantup.com/vmware/downloads


## **Usage**

### **Getting Started**

#### **Clone repo**

```bash
git clone https://github.com/erd0spy/vagrant-ubuntu-desktop-vmware/
cd vagrant-ubuntu-desktop-vmware
```

#### **Customizing VMware settings**

VMX settings and detailed descriptions can be found in the Vagrantfile.


#### **Spinning up environment**

```bash
vagrant up
```

#### **Connecting with SSH**

```bash
PS C:\Users\fikret\Desktop\vagrant-ubuntu-desktop-vmware> vagrant ssh
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.4.0-99-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

 System information disabled due to load higher than 2.0


This system is built by the Bento project by Chef Software
More information can be found at https://github.com/chef/bento
Last login: Fri Feb 11 12:05:39 2022 from 192.168.233.2
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.4.0-99-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

 System information disabled due to load higher than 2.0


This system is built by the Bento project by Chef Software
More information can be found at https://github.com/chef/bento
Last login: Fri Feb 11 12:05:39 2022 from 192.168.233.2
vagrant@vagrant:~$
```

#### **Accessing to the GUI**

Right Click to VMware Tray Icon > Open All Background Virtual Machines

![Desktop](https://github.com/erd0spy/vagrant-ubuntu-desktop-vmware/blob/main/images/desktop.PNG)

#### **Credentials**

- username: `vagrant`
- password: `vagrant`

#### **Vagrant Cloud Repository**

- https://app.vagrantup.com/erd0spy/boxes/vagrant-ubuntu-desktop-vmware
