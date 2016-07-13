# CloudByte CI Modules

**CloudByte CI Modules** repository contains the module files which are helpful in setting up
**OpenStack Continuous Integration environment (CI)**. This environment main purpose is to run a test suite, i.e; **tempest** on top a OpenStack Cinder driver(in this case it is **CloudByte Cinder driver**). This helps in checking the stability and performance of a driver.  

Following are the key modules that will be used for deploying the OpenStack CI:

- **install_master.sh**     : For installing packages for Jenkins Master.
- **install_slave.sh**      : For installing packages for Jenkins Slave.
- **install_log_server.sh** : For installing packages for Jenkins Builds Logs.

## Modules Description

### install_master.sh

This module installs the following packages:

- **Jenkins**.
- **Jenkins Job Builder**.
- **Zuul**.
- **Zuul-merger**.
- **Gerrit Jenkins plugin**.
- **HTTP Proxy settings**.

Also, after installing these packages it grants the Linux OS (on top of which the above packages are installed) the privilege to be used as a **Jenkins Master**.

### install_slave.sh

This module installs the packages which enables the Linux OS to be used as a **Jenkins Slave**.

### install_log_server.sh

This module installs the packages which enables the Linux OS to catch all the logs generated after each build in **Jenkins**.

```
NOTE: Each module should be installed on a separate Linux OS, preferably Ubuntu 14.04.
```


