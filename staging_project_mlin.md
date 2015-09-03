# Get something new everyday
## - Staging Project for openSUSE

Max Lin <mlin@suse.com>


## Introduction
As you know openSUSE introduced Staging Project in the openSUSE Factory development model[1], it is a gate to ensure the package updates will not break Factory, or keep main part of Factory can keep work. openSUSE Factory are received tons of new changes everyday, it also means we often found new problem/bug as well, the Staging Project should(must be) catch those issues in staging period, in this talk, I'll introduce how Staging Project work and how we handle the Staging Project.

## Agenda
* Basic workflow
* What is **adi** staging(NEW)?
* The tools used for Staging Project
* Recognize the quality - by openQA[2]
* Case Study
* Q&A

### Basic workflow
As many of you should already have basic concept of Staging Project on openSUSE, I'll introduce basic workflow of Staging Project quickly in this part.

### What is adi staging?
New toy! The **adi**(Ad Intern) staging project[3] is a kind of temporary staging *non-rings* package's submission, in order to ensure new package or package update can built against Factory, and can pass the repochecker.

### The tools used for Staging Project
Introducing the tools we used for Staging Project[4].

### Recognize the quality - by openQA
Each real staging project(except adi staging project) will generate an test image for testing on openQA, I'll explain how those images generating, and will also explain what parts are covered in current test plan.

### Case Study
I'll show you several bugs what Staging Project caught in the past; some issues what can breaks Staging Project; some cases causes the submission stuck in Staging Project.


[1] [openSUSE Factory development model](https://en.opensuse.org/openSUSE:Factory_development_model)

[2] [openQA](http://os-autoinst.github.io/openQA/)

[3] [Announcement of adi staging](http://lists.opensuse.org/archive/opensuse-packaging/2015-07/msg00073.html)

[4] [osc-plugin-factory](https://github.com/openSUSE/osc-plugin-factory)
