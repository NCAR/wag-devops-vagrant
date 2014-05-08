# ...Vagrant!

- handles: IP, SSH, portability, port-forwarding, file sharing
- provisioner hooks
   - shell
   - Puppet
   - Chef
   - Ansible
   - Salt

!SLIDE

# Vagrant Workflow

## Box Creation

- create VM
  - in **VirtualBox** or other provider's GUI
- configure VM for **Vagrant**
  - install Guest Additions
  - add `vagrant` user w/ `sudo` privilege
- package

  `$ vagrant package --output awesome.box awesome-vm`

<!-- TODO: example commands, optional demo if there's time / interest -->

!NOTE
this is done infrequently

!SLIDE

# Vagrant Workflow

## Box Usage

- box add

  `$ vagrant box add --name awesome-box awesome.box`

- up

  `$ vagrant up`

<!-- TODO: example commands, optional demo if there's time / interest -->

!NOTE
this is done frequently

!SLIDE

# Vagrant Providers

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

\* *via third-party plugins*

<!-- easy for developers to deploy to operational environments -->

!SLIDE

# Vagrant @ EOL

- soon to be one month old <img src='img/cake-48.png' alt='cake!' />
- currently Mike and Erik
- soon other Catalog Developers
- and then other EOL teams, per interest

!SLIDE

# Vagrant @ EOL

- develop base minimal Linux box
  - no provisioners
  - no Ruby, Drupal, etc.

- Development boxes built from minimal Linux box:
  - `catalog-dev`
  - `eol-drupal-dev`

- boxes shared via **NFS**: `/net/vagrant/`

!SLIDE

# Vagrant @ EOL: Benefits

- dramatic time savings
- reproducible development environments
- ...it *just works!*

!SLIDE

# Vagrant @ EOL

## Lessons Learned

- very handy, easy to use
- initial box creation can be laborious
- document actions for others
- script / use provisioners everything for you can for automation, documentation and use by others
- highlights pain points in deployment workflow
- compression of virtual drive files
  - zero out empty space
  - compress w/ virtualization tool, e.g. `VBoxManage modifyhd --compress`

<!-- TODO: try to clean this up -->

!SLIDE

# Vagrant @ EOL: Future

- automate box creation in future w/ `packer.io` and Kickstart file(s)
- propagate usage to other Catalog Developers and other EOL teams, per interest
