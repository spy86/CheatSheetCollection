## DKMS Setup
```shell
    apt-get install build-essential dkms 
```
## Commands

List managed DKMS modules
```shell
    dkms status
```    
List installed DKMS Debian packages
```shell
    dpkg -l "*-dkms"
```
## Build DKMS module from git source

Prepare sources:
```shell
    git clone <some repo> src
    cd src
    NAME=<module name>
    VERSION=<module version>
    mkdir /usr/src/${NAME}-${VERSION}
    git archive driver-${VERSION} | tar -x -C /usr/src/${NAME}-${VERSION}
```
And build using DKMS
```shell
    dkms add     -m ${NAME} -v ${VERSION}
    dkms build   -m ${NAME} -v ${VERSION}
    dkms install -m ${NAME} -v ${VERSION}
```
Finally check if "dkms status" lists the module with state "installed" for your kernel version

## Uninstalling
```shell
    dkms remove <module name>/<module version> --all
```    
