# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  oses = []
  File.open("oses").each_line do |line|
    line.chomp!
    next if line.empty? || line.start_with?('#')
    oses << line
  end
  oses.each do |version|
    config.vm.define version do |os|
      os.vm.box = version
    end
  end
  #config.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
  config.vm.provision "file", source: "test.exe", destination: "test.exe"
  config.vm.network "private_network", type: "dhcp"
end
