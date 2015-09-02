# Get something new everyday
## - Staging Project for openSUSE

Max Lin <mlin@suse.com>

## Introduction
----
As you know openSUSE introduced Staging Project in the openSUSE Factory development model[1], it is a gate to ensure the package updates will not break Factory, or keep main part of Factory can continue work. openSUSE Factory are received tons of new changes everyday, and it also means we often found new problem/bug in the Staging Project. In this talk, I'll introduce how Staging Project work and how we handle the Staging Project.

## Agenda
----
* Basic workflow
* What is **adi** stagings(NEW)?
* Dashboard
* Recognize the quality of stagings can be acceptable - by openQA[2]
* The tools used for Staging Project
* How we handle the Staging Project
* Case Study: the bugs caught in the past
* Q&A

As many of you should already have basic concept of Staging Project on openSUSE, I'll go through the first three parts quick and put more time introducing the tools we using; how the test image generated; what kind of openQA tests runs against stagings. And I'll show you several cases: the bugs that Staging Project caught in the past.


[1] [openSUSE Factory development model](https://en.opensuse.org/openSUSE:Factory_development_model)

[2] [openQA](http://os-autoinst.github.io/openQA/)