MinimalistiCli
==============

Overview
--------

This project serves as an example of command line module (CLI) built against a Slicer build tree.



Checkout, configure and build
-----------------------------

```bash
$ git clone git://github.com/jcfr/MinimalistiCli.git
$ mkdir MinimalistiCli-build
$ cd MinimalistiCli-build
$ cmake -DSlicer_DIR:PATH=/path/to/Slicer-Superbuild-Debug/Slicer-build ../MinimalistiCli
$ make
```

Run 
---

```bash
$ ./lib/Slicer-4.1/cli-modules/MinimalistiCli -r 1 -r 2
3
```

Slicer integration
------------------

### Method 1: Manually edit slicer settings

```bash
$ ./Slicer --settings-path
$ vi /home/jchris/.config/NA-MIC/Slicer.ini
```
As illustrated below, set or update `AdditionalPaths' settings. Note that this a comma separated list.

```
[Modules]
AdditionalPaths=/home/jchris/Projects/MinimalistiCli-build/lib/Slicer-4.1/cli-modules
```


### Method 2: Add module path within *Slicer application settings.*


1. Start Slicer
2. *Edit* -> *Application Settings* -> *Modules settings*
3. Under *Additional module paths*, click on **>>** button, then *Add* the following path:

`/home/jchris/Projects/MinimalistiCli-build/lib/Slicer-4.1/cli-modules`

