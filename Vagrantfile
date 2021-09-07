Vagrant.configure("2") do |config|
    config.vm.define 'ubuntu' do |ubuntu|
        ubuntu.vm.box = "ubuntu/trusty64"
        config.vm.network "public_network"
        config.vm.network "private_network", type: "dhcp"
      end
      
      config.vm.define 'kali' do |kali|
        kali.vm.box = "kalilinux/rolling"
        config.vm.network "public_network"
        config.vm.network "private_network", type: "dhcp"
      end

    # Prevent SharedFoldersEnableSymlinksCreate errors
    config.vm.synced_folder ".", "/vagrant", disabled: true
end
