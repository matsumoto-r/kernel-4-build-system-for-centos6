# Kernel 4.x.y build system for CentOS6 on Vagrant

kernel 4.x.y build server for centos6 created by Vagrant and Itamae

## create build server
```
cd vagrant-build-kernel-centos6
vagrant up
itamae ssh -l debug --vagrant roles/build-kernel-for-cent64.rb
vagrant ssh
ls -l ~/linux-4.1.1
```
