# Kernel {4,3}.x.y build system for CentOS 6

kernel {4,3}.x.y build system for centos 6 created by Vagrant and Itamae

## dependency

- vagrant
- vagrant-persistent-storage
- itamae

You can run setup task below(Vagrant and Ruby/Bundler should be pre-installed, so ask google how):

```
make setup
```

## create build server

- build stable kernel

```
make
```

or 

```
make stable
```

- kernel-4.1.2 or other kernel version

```
make KERNEL_VER=4.1.2
```
```
make KERNEL_VER=3.18.18
```

- use kernel build parameters

```
make KERNEL_VER=4.4.1 KERNEL_BUILD_HOST=matsumoto-r.jp KERNEL_BUILD_USER=matsumotory KERNEL_LOCAL_VER=.matsumotory
```

then, kernel build parameters were changed as the followings:

```
[vagrant@hoge ~]$ uname -r
4.4.1.matsumotory
[vagrant@hoge ~]$ dmesg | grep matsumotory
[    0.000000] Linux version 4.4.1.matsumotory (matsumotory@matsumoto-r.jp) (gcc version 4.4.7 20120313 (Red Hat 4.4.7-3) (GCC) ) #1 SMP Tue Feb 2 20:07:16 JST 2016
```


create rpm into `./build/kernel-{4,3}.x.y`

## confirm the kernel version build completely(2015-12-21)
- 4.3.x
- 4.2.x
- 4.1.x
- 3.18.18
- 3.14.48
- 3.12.44
- 3.10.84

## License
under the MIT License:
- see LICENSE file

