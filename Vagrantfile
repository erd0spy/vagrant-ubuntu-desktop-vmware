Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"                  # select bento/ubuntu-20.04 box
  config.vm.provider "vmware_desktop" do |v|            # select 'vmware_desktop' as provider
    v.vmx['virtualHW.version'] = '16'                   # choose 16 as 'vmware_desktop' version
    v.vmx['mks.enable3d'] = true                        # enable 3D acceleration
    v.vmx['vmci0.present'] = true                       # enable Virtual Machine Configuration Interface
    v.vmx['hpet0.present'] = true                       # enable High Precision Event Timer
    v.vmx['virtualHW.productCompatibility'] = 'hosted'  # select 'virtualHW.productCompatibility' as 'hosted' this simply means we work with VMware Fusion, Workstation, Player etc.
    v.vmx['powerType.powerOff'] = 'soft'                # regular power settings 
    v.vmx['powerType.powerOn'] = 'soft'                 # regular power settings
    v.vmx['powerType.suspend'] = 'soft'                 # regular power settings
    v.vmx['powerType.reset'] = 'soft'                   # regular power settings
    v.vmx['guestOS'] = 'ubuntu-64'                      # select 'ubuntu-64' as 'guostOS' in VMware
    v.vmx['sound.autoDetect'] = true                    # regular sound settings
    v.vmx['sound.fileName'] = '-1'                      # regular sound settings
    v.vmx['sound.present'] = true                       # regular sound settings
    v.vmx['numvcpus'] = '2'                             # two processor cores reserved for vm
    v.vmx['cpuid.coresPerSocket'] = '2'                 # one socket reserved for vm [1(socket)*2(CPU)=2(CPU)]
    v.vmx['vcpu.hotadd'] = true                         # enable VMware Hot Add for CPU              
    #v.vmx['vhv.enable'] = true                         # enable nested virtulazation on vm
    v.vmx['memsize'] = '3072'                           # reserve 3GB RAM for vm
    v.vmx['mem.hotadd'] = true                          # enable VMWare Hot Add for RAM
    v.vmx['nvme0.present'] = true                       # select nvme for primary drive
    v.vmx['usb.present'] = true                         # enable USB controller
    v.vmx['ehci.present'] = true                        # enable USB controller
    v.vmx['svga.graphicsMemoryKB'] = '262144'           # reserve 256MB for GPU
  end

  #config.vm.synced_folder "", ""                       # enable sycned folder for vm

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get full-upgrade -y
    apt-get install tasksel network-manager network-manager-gnome gdm3 open-vm-tools-desktop mate-terminal adwaita-icon-theme-full -y
    tasksel install ubuntu-desktop-minimal -y
    systemctl set-default graphical.target
    reboot
  SHELL
end
