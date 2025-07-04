## Why Linux for Embedded Systems?
There are many reasons for the rapid growth of embedded
Linux. 
To name a few:
- Royalties: Unlike traditional proprietary operating systems, Linux can be deployed without any royalties.
- Hardware Support: Linux supports a vast variety of hardware devices including all major and commonly used CPU architectures: ARM, Intel x86, MIPS, and PowerPC in their respective 32-bit and 64-bit variants.
- Networking: Linux supports a large variety of networking protocols. Besides the ubiquitous TCP/IP, virtually any other protocol on any physical medium is implemented.
- Modularity: A Linux OS stack is composed of many diﬀerent software packages. Engineers can customize the stack to make it exactly ﬁt their application.
- Scalability: Linux scales from systems with only one CPU and limited resources to systems featuring multiple CPUs with many cores, large memory footprints, several networking interfaces, and much more.
- Source Code: The source code for the Linux kernel, as well as for all software packages comprising a Linux OS stack, is openly available.
- Developer Support: Because of its openness, Linux has attracted a huge number of active developers, and those developers have quickly built support for new hardware.
- Commercial Support: An increasing number of hardware and software vendors, including all semiconductor manufacturers as well as many independent software vendors (ISV), are now oﬀering support for Linux through products and services.
- Tooling: Linux provides myriad tools for software development ranging from compilers for virtually any programming language to a steadily growing number of proﬁling and performance measurement tools important for embedded systems development.

and the important thing is that in our graduation project we didn't need to develop the device drivers for UART ,camera and many others and this decreased our development time

## Embedded Versions of Full Linux Distributions
- Debian (www.emdebian.org)
- Fedora (https://fedoraproject.org/wiki/Embedded)Gentoo (https://wiki.gentoo.org/wiki/Project:Embedded)
- SUSE (https://tr.opensuse.org/MicroSUSE)
- Ubuntu (https://wiki.ubuntu.com/EmbeddedUbuntu)

  **and we are working on Ubuntu**

## Embedded Linux Development Tools
- Baserock

    Baserock is an open source project that provides a build system for Linux distributions, a development environment, and a development workﬂow in one package.
    The project’s homepage is at http://wiki.baserock.org.

- Buildroot

    Buildroot is a build system for complete embedded Linux systems using GNU Make and a set of makeﬁles to create a cross-compilation toolchain, a root ﬁlesystem, a kernel image, and a bootloader image. The project’s homepage is at  http://buildroot.uclibc.org.
    Buildroot mainly targets small footprint embedded systems and supports various CPU architectures. To jump start development it limits the choice of conﬁguration options and defaults to probably the most commonly used ones for embedded system.

- OpenEmbedded

    OpenEmbedded (www.openembedded.org) is a build framework composed of tools, conﬁguration data, and recipes to create Linux distributions targeted for embedded devices. At the core of OpenEmbedded is the BitBake task executor that manages the build process.

- The Yocto Project

    **Yocto Project is our subject**. It is listed here to complete this overview of the embedded Linux landscape. 
    You can ﬁnd its webpage at https://www.yoctoproject.org.

## we have to approaches for building our embedded project
- top-down :

    In this approach, you start with one of the many
    available Linux distributions and customize it according to your requirements by adding and/or removing software packages.
    The author took this approach many years ago with a high-speed image processing system running on x86 server hardware. It is a viable approach and has its appeal because using a tested and maintained distribution alleviates some of the more tedious tasks of building and maintaining your own distribution. And you may be able to get support for it.
    However, it may limit you in your choice of hardware, since most oﬀ-the-shelf Linux distributions are built for x86 hardware. And, of course, picking the right distribution to start oﬀ with and rightsizing it for your target device is not that simple either.


- Bottom-up: 

    The bottom-up approach entails building your own custom Linux distribution from source code starting with a bootloader and the kernel and then adding software packages to support the applications for your target device. This approach gives you the most control, but it is also a challenging task. You will have to make many choices along the way, from selecting the right toolchain and setting kernel conﬁguration options to choosing the right software packages. Some of these choices are interdependent, such as the choice of toolchain and target library, and taking the wrong turn can quickly send you
    down a dead end. After you have successfully built and deployed your own distribution, you are left with the burden of maintaining it—ﬁnding patches and security updates for the kernel and all the other packages you have integrated with your distribution.

    This is where the strengths of the Yocto Project lie. It combines the best of both worlds by providing you with a complete tool set and blueprints to create your own Linux distribution from scratch starting with source code downloads from the upstream projects. 
    The blueprints for various systems that ship with the Yocto Project tools let you build complete operating system stacks within a few hours. 
    You can choose from blueprints that build a target system image for a basic system with command-line login, a system with a graphical user interface for a mobile device, a system that is Linux Standard Base compliant, and many more.

    You can use these blueprints as a starting point for your own distribution and modify them by adding and/or removing software packages.

