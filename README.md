# allocator
Homework 03 task. [OTUS C++]

[![Build Status](https://travis-ci.org/DGolgovsky/allocator.svg?branch=master)](https://travis-ci.org/DGolgovsky/allocator)
[![Code Health](https://landscape.io/github/DGolgovsky/allocator/master/landscape.svg?style=flat)](https://landscape.io/github/DGolgovsky/allocator/master)
[ ![Download](https://api.bintray.com/packages/dgolgovsky/otus-cpp/allocator/images/download.svg) ](https://bintray.com/dgolgovsky/otus-cpp/allocator/_latestVersion)

Implementation of custom memory allocator, which will allow the reserve operation for the `std::map` container. The allocator parameterized the number of elements selected at a time.
Exemption of a specific element is not expected - the allocator release all memory self.
Implemented own container, which by analogy with stl containers is parametrized by the allocator.

The application code contain the following calls:

• creating an instance of std::map

• filling with 10 elements, where the key is a number from 0 to 9, and the value - factorial of a key

• creating an instance of std::map with a new allocator limited to 10 elements

• filling with 10 elements, where the key is a number from 0 to 9, and the value - factorial of a key

• display all values (key and value are separated by a space) stored in a container

• creating an instance of its container to store int

• filling with 10 elements from 0 to 9

• creating an instance of its container to store int with the new allocator with limited 10 elements

• filling with 10 elements from 0 to 9

• Display all values stored in the container

**Example of Dockerfile**

```
FROM ubuntu:trusty
#### Bintray (by JFrog) <bintray@bintray.com>
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 379CE192D401AB61
#### Dmitry Golgovsky (Packages sign) <d.westcoast@aol.com>
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys D5CEB8D4D5185900
#### toolchain repo key
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 1E9377A2BA9EF27F
RUN echo "deb http://dl.bintray.com/dgolgovsky/otus-cpp trusty main" | sudo tee -a /etc/apt/sources.list
RUN echo "deb http://ppa.launchpad.net/ubuntu-toolchain-r/test/ubuntu trusty main" | sudo tee -a /etc/apt/sources.list
RUN apt update
RUN apt install -y libstdc++6 allocator
```

# OTUS-Cpp
OTUS C++ online [course](https://otus.ru/lessons/razrabotchik-c++/) studying repository.

**About the course**

Being one of the most popular programming languages, C++ is widely used for software development. Scope of usage includes the creation of operating systems, a variety of applications, device drivers, applications for embedded systems, high-performance servers, and entertainment applications (games).
In the course "C++ Developer" will be considered as introductory concepts, such as automation tools, STL, innovations of `11` and `14` standards; and more complex: asynchronous programming, design patterns, distributed high-availability services architectures.
