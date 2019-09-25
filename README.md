# MUMPS Examples

**MUMPS** ("Massachusetts General Hospital Utility Multi-Programming System"), or **M**, is a general-purpose computer programming language originally designed in 1966 for the healthcare industry. Its differentiating feature is its "built-in" database, enabling high-level access to disk storage using simple symbolic program variables and subscripted arrays; similar to the variables used by most languages to access main memory. [Read more...](https://en.wikipedia.org/wiki/MUMPS)

The implementations currently available are:

- [Intersystems (Caché)](http://www.intersystems.com/)
- [FIS (GT.M)](http://www.fisglobal.com/products-technologyplatforms-gtm)
- [MUMPS Database and Language by Ray Newman](http://sourceforge.net/projects/mumps/)
- [Open Mumps](http://www.cs.uni.edu/~okane/)

The examples in this tutorial are run with both GPL Mumps and GT.M.

## Prerequisites

### GPL Mumps

- [The Mumps Programming Language](https://www.cs.uni.edu/~okane/)
- [Mumps Language Users' Guide](https://www.cs.uni.edu/~okane/source/MUMPS-MDH/ReadMe.pdf)
- [Mumps Language Quick Introduction & Tutorial](https://www.cs.uni.edu/~okane/source/MUMPS-MDH/MumpsTutorial.pdf)

### GT.M

- [MUMPS Technology Portal](http://mumps.cz/)

---

## Quick Setup

### GPL Mumps

To install the open source distribution of the Mumps interpreter:

    cd /usr/local/src
    wget https://www.cs.uni.edu/~okane/source/MUMPS-MDH/mumps-18.02.src.tar.gz
    tar -zxvf mumps-18.02.src.tar.gz
    cd mumpsc
    ./ConfigureNative.script
    ./BuildMumpsWithGlobalsInSingleUserNative.script

The resulting interpreter is located in `/usr/bin/mumps`.

    mumps

    Mumps 17.30; Built: 16:05:53 Sep 23 2019
    Float: double; DBMS: Native Stand Alone; Hardware math: yes; Int: int; Float digits: 6; Cache: 33; Block: 2048; FP Bits: N/A
    http://threadsafebooks.com/
    Enter HALT to exit

    > write "Hello world"
    Hello world
    > halt
    EOF - goodbye ...

To uninstall GPL Mumps:

    cd /usr/local/src/mumpsc
    make uninstall
    rm -f /usr/bin/mumps*

### GT.M

To install GT.M on Debian based OS:

    apt-get install fis-gtm

Set up the environment variables:

    source /usr/lib/x86_64-linux-gnu/fis-gtm/V6.3-003A_x86_64/gtmprofile

Open the GT.M prompt:

    gtm

    GTM>write "Hello world"
    Hello world
    GTM>halt

To uninstall GT.M:

    apt-get purge fis-gtm

---

## 1. The Very Basics

### [`01-hello-world.mps`](https://github.com/programarivm/gpl-mumps-by-example/blob/master/01-the-very-basics/01-hello-world.mps)

    Hello world

### [`02-hello-world-in-a-loop.mps`](https://github.com/programarivm/gpl-mumps-by-example/blob/master/01-the-very-basics/02-hello-world-in-a-loop.mps)

    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world

### [`03-hello-world-in-another-loop.mps`](https://github.com/programarivm/gpl-mumps-by-example/blob/master/01-the-very-basics/03-hello-world-in-another-loop.mps)

    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world
    Hello world

### [`04-hello-world-in-a-nested-loop.mps`](https://github.com/programarivm/gpl-mumps-by-example/blob/master/01-the-very-basics/04-hello-world-in-a-nested-loop.mps)

    1:1 Hello world
    1:2 Hello world
    1:3 Hello world
    1:4 Hello world
    1:5 Hello world
    2:1 Hello world
    2:2 Hello world
    2:3 Hello world
    2:4 Hello world
    2:5 Hello world

### [`05-arithmetic-operations.mps`](https://github.com/programarivm/gpl-mumps-by-example/blob/master/01-the-very-basics/05-arithmetic-operations.mps)

    There were 7 apples, 8 pears and 9 oranges,
    a total of 24 fruits in a basket.
    Then, something happened:
    1 apple, 2 pears and 0 oranges were eaten!
    Now there are 21 fruits in the basket,
    the average fruit value is 7.

### [`06-arrays.mps`](https://github.com/programarivm/gpl-mumps-by-example/blob/master/01-the-very-basics/06-arrays.mps)

    Approaching the solar system:
    Mercury
    Venus
    Earth
    Mars
    Jupiter
    Saturn
    Uranus
    Neptune
    Pluto

    September 2019:
    26 27 28 29 30 31 1
    2 3 4 5 6 7 8
    9 10 11 12 13 14 15
    16 17 18 19 20 21 22
    23 24 25 26 27 28 29
    30 1 2 3 4 5 6

    Genealogical tree:
    Harry and Emily had Jack

    Associative array:
    Have you ever been to London?

## 2. User Defined Functions

### [`01-factorial-by-reference.mps`](https://github.com/programarivm/gpl-mumps-by-example/blob/master/02-user-defined-functions/01-factorial-by-reference.mps)

    Enter n: 5
    5! = 120

---

### Contributions

Would you help make this tutorial better? Contributions are welcome.

- Feel free to send a pull request
- Drop an email at info@programarivm.com with the subject "Open MUMPS by Example"
- Leave me a comment on [Twitter](https://twitter.com/programarivm)
- Say hello on [Google+](https://plus.google.com/+Programarivm)

Many thanks.
