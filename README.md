# VBOX-DEV-INFRA

#### Prerequisites:
Following softwares must be up & running on the host machine as a pre-requisite:
1. Vagrant
2. VirtualBox

#### Softwares installed on Guest OS
1. Ansible
2. Docker
3. pip & certain libraries
4. CouchBase (as a Docker container)
5. Elastic server (as a Docker container)
6. Java 8 (JDK)
7. Zk-Kafka single node setup
8. Spark server (TODO)

#### Steps:
1. From the project's root directory, execute 
    > vagrant up
    
    This is going to take some time when you run it for the first time as Guest OS, Docker, docker images and other software & dependencies will be downloaded.
    On completion you will get a message ```The dev infra is up!```

2. > vagrant ssh

    You can log into the guest OS and play around
    
3. Now you can access the softwares exposed from your host OS using IP ```192.168.32.10```. 
   Or add it to your /etc/hosts file.



