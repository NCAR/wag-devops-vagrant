# ...Vagrant!

- things that it handles: IP, SSH, portability, etc.
- provisioner hooks
   - shell
   - Puppet
   - Chef
   - Ansible
   - Salt

!SLIDE

# Vagrant Workflow

- create VM
- package
- box add
- up

<!-- TODO: example commands, optional demo if there's time / interest -->

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

- soon to be one month old
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

# Vagrant @ EOL: Lessons Learned

- very handy, easy to use
- initial box creation can be laborious
- document actions for others
- script / use provisioners everything you can for automation and others
- compression of virtual drive files
  - zero out empty space
  - compress w/ virtualization tool, e.g. `VBoxManage modifyhd --compress`
- highlights pain points in deployment workflow

<!-- TODO: try to clean this up -->

!SLIDE

# Vagrant @ EOL: Future

- automate box creation in future w/ `packer.io` and Kickstart file(s)
- propagate usage to other Catalog Developers and other EOL teams, per interest
