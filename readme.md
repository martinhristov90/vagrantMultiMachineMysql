## This repository provides a simple Vagrantfile to use with Vagrant, providing multi-machine setup and MySQL server.

## How to install Vagrant :

- Information about installing Vagrant can be found on the official HashiCorp website [here](https://www.vagrantup.com/docs/installation/)

## How to use it :

- In a directory of your choice,clone the github repository with `git clone https://github.com/martinhristov90/vagrantMultiMachineMysql.git`
- Change into the directory using : `cd vagrantMultiMachineMysql`
- Execute `vagrant up`
- It might take some time to download the boxes since you do not have them added to Vagrant.
- Check with `vagrant status` that you have both Vagrant boxes running. The output should look like this:
```shell

TO BE FILLED

```

- To stop the running machines execute `vagrant halt`, to destroy the setup use `vagrant destroy`.