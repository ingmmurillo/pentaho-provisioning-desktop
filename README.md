# Provisioning Pentaho v8.2 CE Tools on Ubuntu Desktop v18.04 LTS - [DEV Environment]
The following code automates the procedure to install and configure on an operating system Ubuntu Desktop v14.08 LTS the following software:

* [**OpenJDK 8**](https://openjdk.java.net/install/)
* [**PostgreSQL Server Database**](http://www.postgresql.org/download/)
* [**SQL Power Architect v1.0.8 Community Edition**](http://www.sqlpower.ca/page/architect_download_os)
* [**DataCleaner v5.7.0**](https://datacleaner.github.io/downloads)
* [**SQuirreL SQL Client v3.9.1**](https://sourceforge.net/projects/squirrel-sql/files/1-stable/)
* [**Pentaho Data Integration v8.2**](https://sourceforge.net/projects/pentaho/files/Pentaho%208.2/client-tools/)


This **[IAC](http://martinfowler.com/bliki/InfrastructureAsCode.html)** (Infrastructure as Code) allows you to have **Pentaho & Open Source Data Tools** on an Ubuntu Desktop, it is ideal to start developing Data Warehousing / Business Intelligence systems.

Before using this code, make sure you have installed the following packages in your MAC:

* [**Ansible**](http://docs.ansible.com/ansible/intro_installation.html)
* [**Vagrant**](https://www.vagrantup.com/docs/installation/)
* [**VirtualBox**](https://www.virtualbox.org/)
* [**Wget**](https://www.gnu.org/software/wget/)

Create the directory **./files** and have downloaded the following packages
```sh-session
files
│   ├── jdbc
│   │   └── postgresql-42.2.6.jar
│   └── tools
│       ├── DataCleaner-5.7.0.zip
│       ├── SQL-Power-Architect-generic-jdbc-1.0.8.tar.gz
│       ├── pdi-ce-8.2.0.0-342.zip
│       └── squirrelsql-3.9.1-standard.zip
```

Open a terminal console and install the following roles:
```sh-session
ansible-galaxy install geerlingguy.java
ansible-galaxy install geerlingguy.postgresql
```

Finally, run the provisioning code with the following command:
```sh-session
vagrant up
```

**NOTES:**
* Just the first time you run the command, it will take some minutes
* [**Ansible**](http://www.ansible.com/) and [**Vagrant**](http://www.vagrantup.com/) runs well on Linux distributions and OS X. To run those on Windows is tricky, but not impossible
* The user and password for the box are **vagrant**