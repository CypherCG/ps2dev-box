A Virtual Machine for PS2 Development
=====================================

To give you a little bit of background, you may want to read these blog posts:

- [Building a Vagrant Box for PS2 Development][blog-1]
- [System Provisioning with Vagrant][blog-2]

## Requirements

- The virtual machine runs on top of [VirtualBox].
- [Vagrant] is used to build and provision the virtual machine.
- [vagrant-omnibus] is required to install Chef inside the VM.
- [Berkshelf] is used to install Chef cookbooks.

## How to build the VM

    $ git clone git://github.com/mlafeldt/ps2dev-box.git
    $ cd ps2dev-box/
    $ bundle install
    $ bundle exec berks install --path vendor/cookbooks
    $ vagrant up --provision

That's it.

(You can edit the `Vagrantfile` to let Vagrant provision a different VM or to
use the Shell provisioner instead of Chef Solo.)

## Contact

* Web: <http://mlafeldt.github.com/ps2dev-box>
* Mail: <mathias.lafeldt@gmail.com>
* Twitter: [@mlafeldt](https://twitter.com/mlafeldt)


[Berkshelf]: http://berkshelf.com/
[Vagrant]: http://vagrantup.com/
[VirtualBox]: https://www.virtualbox.org/
[blog-1]: http://mlafeldt.github.com/blog/2012/06/building-a-vagrant-box-for-ps2-development/
[blog-2]: http://mlafeldt.github.com/blog/2012/08/system-provisioning-with-vagrant/
[vagrant-omnibus]: https://github.com/schisamo/vagrant-omnibus
