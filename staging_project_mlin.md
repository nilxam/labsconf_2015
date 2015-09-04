# Get something new everyday
## - Staging Project for openSUSE

Max Lin <mlin@suse.com>

## Introduction
As you know openSUSE introduced Staging Project in the openSUSE Factory development model[1], it is a gate to ensure new changes will not breaking Factory too much, and it is an important part that we can perform a rolling release distribution of openSUSE - Tumbleweed. openSUSE Factory are received tons of new changes everyday, new changes often brings many new features and new fixes, but it also could means we can found new problem/bug as well, especially a core package change is deemed to have the potential to break so much in Factory, the Staging Project should(must be) catch those issues, and block bad requests merge to Factory till developer fix the breakage.

### Basic workflow
The basic workflow of Staging Project as this picture shown[2].

### What is adi staging?
New toy! The **adi**(Ad Intern) staging project[3] is a kind of temporary staging for *non-rings* package's submissions, in order to ensure new package or package updates can built and did not affect rings, and the requests also can pass the repochecker.

### The tools are involved in Staging Project
We're several tools[4] are involved in Staging Project.

* dashboard - showing the staging projects and their health status.
* osc staging command - handling Staging Project work, adding/removing/moving the request in Staging Project.
* osc check_repo command - mainly detecting file conflicts; package requirements is fulfilled.
* create_test_dvds.sh - create the kiwi file and update to each staging project in order to generate iso file according to the kiwi file.

### Recognize the quality - by openQA
Each real staging project(except adi staging project) will generating an test image in order to testing on openQA[5], currently each staging project need to pass the tests below as successfully before accpet every packages in this staging project to Factory.

* Normal installtion
* Installation with RAID partition sets
* Installation with cryptlvm enabled
* Installation on UEFI
* Can boot after the system installed by above
* MinimalX/GNOME/KDE environment
* Update system to current staging

### Case Study
Show several bugs what Staging Project caught in the past; some issues what have been break Staging Project; some cases causes the submission stuck in Staging Project.


[1] [openSUSE Factory development model](https://en.opensuse.org/openSUSE:Factory_development_model)

[2] [Staging Project workflow](https://progress.opensuse.org/attachments/download/1384/factory_tools.png)

[3] [Announcement of adi staging](http://lists.opensuse.org/archive/opensuse-packaging/2015-07/msg00073.html)

[4] [osc-plugin-factory](https://github.com/openSUSE/osc-plugin-factory)

[5] [openQA](http://os-autoinst.github.io/openQA/)
