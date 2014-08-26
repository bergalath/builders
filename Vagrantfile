# -*- mode: ruby -*-
# vi: set ft=ruby :

script = <<SCRIPT
  sudo apt-get update
#  sudo apt-get upgrade -y # usefull ?
  sudo apt-get install -y subversion python intltool wget build-essential bison flex vim bc
  svn checkout --quiet http://alt-f.googlecode.com/svn/trunk/ alt-f-read-only
  cd alt-f-read-only/alt-f/
  source exports dns325
  make
SCRIPT

Vagrant.configure('2') do |config|
  config.vm.box      = 'hashicorp/precise32'
  config.vm.hostname = 'alt-f.builder'
  config.vm.define     'Alt-f'
  config.vm.provision  'shell', inline: script
end
