# has

`has` helps you check presence of various command line tools and their versions on path.

## How ?

Download the `has` file. There is no dependency apart from `bash` itself 

    $ has node npm java git gradle 
    ✔ node 8.2.1
    ✔ npm 5.3.0
    ✔ java 1.8.0
    ✔ git 2.14.1
    ✔ gradle 4.0.1

If everything is good `has` exists with status code `0`. The status code 
reflects number of commands **not found** on your path.  

    $ has node go javac
    ✔ node 8.2.1
    ✔ go 1.8.3
    ✘ javac

And echo the status:

    $ echo $?
    1


## Installing

Just download the `has` script in your path. 

    git clone https://github.com/kdabir/has.git && cd has && make install


If you are lazy, you can run `has` directly off the internet as well:

    curl -sL https://git.io/_has | bash -s git node npm
    ✔ git 2.14.1
    ✔ node 8.2.1
    ✔ npm 5.3.0


And if that's too much of typing every time, setup an alias
    
    alias has="curl -sL https://git.io/_has | bash -s"

And uses it

    $ has git
    ✔ git 2.14.1


### ♥

[![Build Status](https://travis-ci.org/kdabir/has.svg?branch=has)](https://travis-ci.org/kdabir/has)


## Demo 

[![asciicast](https://asciinema.org/a/135790.png)](https://asciinema.org/a/135790)
