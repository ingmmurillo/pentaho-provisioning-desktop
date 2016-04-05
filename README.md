# Provisioning Pentaho v5.4 CE Tools on Ubuntu Desktop v14.04 LTS - [DEV Environment]
The following code automates the procedure to install and configure on an operating system Ubuntu Desktop v14.04 LTS the following software:

* [**Oracle JDKv7**](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [**PostgreSQL Server Database**](http://www.postgresql.org/download/)
* [**SQL Power Architect v1.0.8 Community Edition**](http://www.sqlpower.ca/page/architect_download_os)
+ [**DataCleaner v4.5**](https://sourceforge.net/projects/datacleaner/)
* [**Pentaho Data Integration v5.4**](https://sourceforge.net/projects/pentaho/files/Data%20Integration/5.4/)
* [**Pentaho BI Server v5.4**](http://sourceforge.net/projects/pentaho/files/Business%20Intelligence%20Server/5.4/)
* [**Pentaho Schema Workbench v3.10.0.1**](https://sourceforge.net/projects/mondrian/files/schema%20workbench/3.10.0/)


This **[IAC](http://martinfowler.com/bliki/InfrastructureAsCode.html)** (Infrastructure as Code) allows you to have **Pentaho Tools** on an Ubuntu Desktop, it
is ideal for start developing with the tools from the stack.

Before using this code, make sure you have installed the following:
* [**Ansible**](http://docs.ansible.com/ansible/intro_installation.html)
* [**Vagrant**](https://www.vagrantup.com/docs/installation/)
* [**VirtualBox**](https://www.virtualbox.org/)
* [**Wget**](https://www.gnu.org/software/wget/)

To run the provisioning code, open a terminal console and run:
```sh-session
vagrant up
```

**NOTES:**
* Just the first time you run the command, it will take some minutes
* [**Ansible**](http://www.ansible.com/) and [**Vagrant**](http://www.vagrantup.com/) runs well on Linux distributions and OS X. To run those on Windows is tricky, but not impossible!
* Create the directory **/files**, download the tools on it and start provisioning it
