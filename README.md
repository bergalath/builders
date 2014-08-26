alt-f.builder
=============

A Vagrantfile to build a VM with all the necessary tools to
cross-compile the Alt-F NAS firmwares and packages.

## BEWARE !
## NOT YET READY TO ROLL !

Based on the instructions from the Alt-F Wiki :
- [Build RC4](http://sourceforge.net/p/alt-f/wiki/How%20to%20Build%20RC4/)
- [Create Packages](http://sourceforge.net/p/alt-f/wiki/How%20to%20Create%20Packages/)

Issues discovered so far :
- The `at` package v3.1.14 has been yanked from debian repo. We must change the version to 3.1.15 in the /[repo]/package/at/at.mk file
- The needed package to compile : subversion python intltool wget build-essential bison flex bc [vim]
- Also needed Ubuntu packages ? : git gnupg gperf build-essential zip curl libc6-dev

The VM creation is pretty fast compared with the first `make` execution  (± 75min on my 2012 Core-i5 laptop)

Downloading stuff takes time …

I should try to create a Vagrant box straigth after the first build !

## Alt-F is released under the terms of the GPLv2
