

- DevOps
  - definition
     - CAMS
     - benefits
  - Virtualization
    - Virtualization Is Awesome!
        - replicate Production environment in Development environment
        - use any host OS for Development environment
           - developer can run their choice of Linux, OSX, Windows
        - set up and share VM means developers can set up new Development
        environment in minutes, not hours or days
     - Virtualization Is A Pain (To Set Up By Hand)
        - install from .iso
        - configure networking
        - determine IP address
        - set up passwords and SSH keys
        - install and configure software
        - ad-hoc sharing w/ others

- ... Vagrant!
  - things that it handles: IP, SSH, portability, etc.
  - provisioner hooks
     - shell
     - puppet
     - chef
     - ansible
     - salt
  - workflow
     - create VM
     - package
     - box add
     - up
  - providers
     - VirtualBox
     - MS HyperVisor
     - MS Azure*
     - VMWare Workspace, Fusion
     - VMWare VSphere*
     - AWS*
     - OpenStack*
     - Docker*
     - ...
     https://github.com/mitchellh/vagrant/wiki/Available-Vagrant-Plugins#providers
     - * Third-Party Plugins
  - Vagrant @ EOL
  - not even one month old
  - sl65-minimal =>
     - catalog development
     - drupal development
  - /net/vagrant/

