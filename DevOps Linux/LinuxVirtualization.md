### Misc

-   [AWS - Using Chef to manage EC2
    instances](http://gerhardlazu.com/2010/08/using-chef-to-manage-amazon-ec2-instances-part1/)
-   [Control Groups](https://lwn.net/Articles/604609/): Detailed LWN
    article

#### Detect VM

[Detect if you are in a virtual
machine](http://people.redhat.com/~rjones/virt-what/)

    virt-what

#### Test for HW virtualisation

    egrep --color "svm|vmx" /proc/cpuinfo

    # svm flag for AMD V
    # vmx flag for Intel VT

#### Image Building Solutions

-   [packer.io](https://www.packer.io) - builds EC2, DigitalOcean, GCE,
    QEMU, VirtualBox, VMWare
-   [Veewee](https://github.com/jedi4ever/veewee) - (Ruby) builds
    Vagrant boxes, KVM, VirtualBox and VMWare images
