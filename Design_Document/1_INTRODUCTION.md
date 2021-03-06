# PegasOS - Introduction

![1 - Introduction](images/1_Introduction/1_image1.png "1 - Introduction")

## 1.1 Executive Summary

Operating Systems are amazing pieces of software. They are something that many of us take for granted in the modern digital age, and yet the amount of work that goes into a functional operating system, let alone a fully-featured and usable operating system is a monument to the decades of design and progress that has gone into the field. From the early days of operating systems that had no display or interface whatsoever, to the early text-based systems, to rudimentary graphic interfaces and finally the modern systems that we are used to - immense amounts of work have gone into optimizing these systems, and making the design as intuitive to the user as possible.

And just as operating systems are amazing pieces of software, they are nothing without the incredible hardware that they run on. We are truly lucky to live in an age with such a wide array of computers to choose from; from powerful full-sized tower PCs to slim and elegant Macbooks, credit-card sized Single-Board Computers and everything in between. Of particular note is the ever-growing field of Single-Board Computers, which contains processing power that blows away anything from as early as 10 years ago for the form factor. No discussion about Single-Board Computers can be complete without the mention of what is perhaps the most significant contributor to the field: the Raspberry Pi.

First released in February of 2012, the small computer boasted 256Mb of RAM, a 700MHz processor, 2 USB 2.0 Ports, a 3.5mm Jack, an HDMI port, and a 250MHz VideoCore IV GPU - all for the low price of $35. It was immediately popular and has become a staple of early computing education and Linux education ever since. The low cost of the computer for them power that it provides allows for a wide array of applications, and many choose to use them as cheap Linux machines as a result.

However, we have a different plan in mind: developing a new operating system specifically for the Raspberry Pi Model 4, and using our development process as a guide for others interested in the world of systems software and operating system development. This new operating system will make as much use out of the hardware as is possible, to show what the Pi 4 can really do. This new operating system is called:

PegasOS.

## 1.2 Personal Motivation/Interests

System software is one of the branches in computer science that has interested me ever since I started my computer science degree. I’d always been interested in both hardware and software and the field of system software was a nice mix of both hardware and software. I’d also wanted to expand my knowledge of the area in system software and joining this project seemed like an excellent opportunity to learn more about operating systems and system software.

- Jacob Thomas


Up until recently, I had wondered what kind of specialization I’d want to have within Computer Science, and never really had a preference. But after taking a lot of time with the Systems Software class that’s offered here at UCF, I began to really appreciate how the software interacts with the hardware, and what kinds of crazy optimizations and algorithms are running behind the scenes to make that happen. Eventually, I decided that I wanted to go above and beyond within the realm of Systems Software, and try doing the most challenging problem in that realm: building an OS from scratch. It’s going to be an amazing learning experience, and a great project to be able to point to and say “We made that from the ground up!”. There’s just so much potential with PegasOS that it makes me very excited to be actually working on it.

- Christopher Walen


Having been in the CS program and to be coming into my 4th year it has finally hit me that the vast majority of software engineer positions are dealt with website development/maintenance and dealing with Full Stack components, like front-end and back-end development. This was made even more clear when a good majority of the senior design pitches were Web Dev. and none of them I found interesting until our PM Chris pitched his idea. The main reason I chose to tackle this great idea of a project is because I wanted to help create some products that will be used for others, monetarily or educationally. The thing with Websites these days is that a vast majority of companies don't make it past their 2nd year or sustain long enough past 10 years. With this project I felt that I could contribute to creating an OS that could be later optimized for the Raspberry Pi and which will lead to better projects being created using the Pi. Also another reason I chose to tackle this project is that I wanted to “get my feet wet” in this area of CS. The concept and execution of operating systems have always intrigued me and I thought “why not learn from the ground up and help create one for others to use”.

- Giancarlo Guillen


I have been working with a lot of high-level gaming software for quite some time, but I always had an interest in the lower-level side of things. I really enjoyed Systems Software and after building my first computer I wanted to learn more about how software interacts with the hardware to make an interface anyone can understand. I have also been working with a lot of low-level programming recently and thought this would be a great way to expand my skill set.
- Jacqueline Godier


Ever since I took system software at UCF my interest on how software interacts with hardware grew from there. Almost all of the project pitches in senior design played out similarly as most of them had vague demands on what the end product should be and many of them didn’t really interest me. The PegasOS project was one of few that was different from the rest of the projects and I think it’s a good opportunity to really understand operating systems and gain more knowledge about system software.

- Kenny Alvarez

## 1.3 Broader Impacts

PegasOS is about creating a brand new operating system for the Raspberry Pi, one of the first mainstream and affordable Single Board Computers on the market. For a low $30-35, you have a surprisingly powerful computer that can fit the niche for a number of projects that require a dedicated computer you might otherwise not have. However, there is already a number of operating systems available for the Raspberry Pi. Why bother with this gargantuan task? What purpose does it serve? This requires a little bit of explanation.

More and more operating systems are becoming available for the Raspberry Pi. Traditionally, when we look at desktop or laptop computers, there are three main choices for operating systems: Windows, Mac, and Linux. Windows and Mac are self-explanatory, as they are very popular options for computer operating systems. Linux is rather complicated for a novice. Linux operating systems are made up of three pieces: the Linux Kernel, the Distribution, and the Desktop Environment. When you hear about OS’s like Debian, Ubuntu, Arch, Kali, and so on, those are what we call distributions of Linux. All that means is that the heart of the OS is the Linux Kernel, and then the rest of the system’s programs, functions, and management are built around that in various ways. Packaged together, this makes a distribution. Sitting on the very top of this, is the Desktop Environment, which is essentially the GUI interface that makes working with the OS that much easier. That is great and all, but how does that relate to the Raspberry Pi?

Raspberry Pi’s are essentially Linux machines. While Windows does have a modified Windows 10 compiled for the Raspberry Pi and a few other SBCs, just about every OS for the Pi is Linux-based. There are exceptions to this, namely the UNIX-based OS’s like RISC OS, OpenBSD, Android, and ChromiumOS (among others), but the overwhelming majority is some form of Linux distribution. Perhaps the most popular option among the Linux distributions is that of Raspbian, which is a Debian-based distribution rewritten specifically for the Pi by the Pi Foundation. It is a 32-bit operating system that comes pre-baked with an LXDE Desktop Environment, featuring options for pre-installed programs or more lightweight offerings. We could go on about the various distributions that are available to the Pi. However, like Raspbian here, the majority are written and compiled to 32-bit mode. This may not seem significant, until you consider the fact that since as early as the later models of Raspberry Pi 2, that the Pi has had an ARM chip containing 64-bit support.

The later Pi 2’s and the standard Pi 3 models contain the model BCM2837 processor. This processor contains a Quad-Core ARM Cortex A53 at 1.2Ghz, which supports ARMv8 - a 64-bit instruction set. The Pi 3A+ and 3B+ contain a model BCM2837B0 processor, which also contains a Quad-Core ARM Cortex A53 with a higher frequency of 1.4Ghz - meaning this also supports ARMv8. Lastly, the Pi 4 contains a model BCM2711, which contains a Quad-Core ARM Cortex A72 at 1.5Ghz - making it the fastest processor of the bunch that also supports ARMv8.

The majority of operating systems for the Pi contain either ARMv6 or ARMv7 instruction sets, which are backward-compatible with ARMv8. This makes it an ideal choice as far as portability is concerned because the old Pi 1/2/Zero models do not support ARMv8, so having your distribution compile to 32-bit and simply telling the newer models to run in 32-bit mode means you can keep versions across all the Pi’s and leave no one out. However, if you are running these processors in 32-bit mode by using the ARMv6 or ARMv7 instruction set, you are simply wasting the instruction space that the processor is giving you, which is a greatly missed opportunity that is ever-so-slowly being capitalized on.

And this is where PegasOS comes in. Our goal is to make a true 64-bit, ARMv8 OS for the Raspberry Pi, and since this is compiling to ARMv8, potentially any machine that runs a 64-bit ARM processor could run this OS as well. We want to make the most use of the processor that the hardware is giving us, and to use that to write a fast and efficient OS that offers something a bit apart from the standard Linux and UNIX systems.

Because PegasOS will be FOSS (Free and Open Source Software) at the end of the project, it will be publicly available for anyone who wants to use it or build on to it. The GitHub repositories are already public and can be forked or pulled to for other contributors past the scope of the project during this Spring/Fall term. In conjunction with our requirements for our capstone here at UCF, the amount of documentation that will go along with the building of this OS will serve as an educational tool for those interested in systems software and operating systems development, of which there is a lack of sources in this regard apart from wiki.OSDev.org. While on this journey of building PegasOS, there are also opportunities to create new and improved algorithms related to OS development, that could be used in other OS projects. The PegasOS team believes that Systems Software is incredibly engaging, challenging, and rewarding as a result, and we want to share that with others out there that have that same spark that we all have.

[Back - Design Document Home](DESIGN_DOCUMENT.md) | [Next - Legal, Ethical, and Technical](2_LEGAL_ETHICAL_TECHNICAL.md) | 
[Design Document Home](DESIGN_DOCUMENT.md) | [Documentation Home](../README.md)