
# This repo is deprecated

See https://github.com/cloudius-systems/osv-apps/tree/master/erjang


osv-erjang
==========

Erjang (Erlang for JVM) [1] running on OSv [2].

Please install `capstan` tool first [3,4].
Its somewhat similar to using `Dockerfile`s with `docker` CLI tool.

NOTE: for now its just uses a pre-built `erjang-R16B01.jar`.
The proper way should be to add `Capstanfile` to erjang repo.

How to run:

1. install `qemu` on Linux or `VirtualBox` on other platforms.

2. install `capstan`.

3. Run:
    ``` bash
    $ git clone git@github.com:nivertech/osv-erjang.git
 	$ cd osv-erjang/
    
    $ capstan build
	Building osv-erjang...
	
	$ capstan run
	Created instance: osv-erjang
	OSv v0.08
	** Erjang R16B01 **  [root:/~resource] [erts:5.10.2] [smp S:1 A:10] [java:1.7.0_51] [unicode]
	Eshell V5.10.2  (abort with ^G)
	1> lists:reverse("Hello, world!").
	"!dlrow ,olleH"
	2> ^C
	$ 
    ```


[1] A JVM-based Erlang VM:
- http://www.erjang.org
- https://github.com/trifork/erjang

[2] OSv
- http://osv.io

[3] Capstan:
- http://osv.io/capstan/
- https://github.com/cloudius-systems/capstan

[4] Capstan Java example:
- https://github.com/cloudius-systems/capstan-example-java
