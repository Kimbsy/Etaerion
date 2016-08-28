# Etaerion

```
Etaerio - noun
    An aggregate fruit, as one consisting of drupes (e.g. raspberry)
```
## Overview
The purpose of the Etaerion project is to learn about clustered supercomputer architecture and how to write highly parallelised programs to take advantage of it.

This will be acheived by cerating a [Beowulf cluster](https://en.wikipedia.org/wiki/Beowulf_cluster) using Raspberry Pi Zero single board computers, this cluster can then be used to run parallelised programs.

## Hardware
The Etaerion supercomputer will be a cluster of 8 Raspberry Pi Zero client nodes controlled by a Raspberry Pi 3 Model B server node.

```
                                           ╔════════╗
                                           ║ Node 0 ║
                                           ║ RPi 3  ║
                                           ╚═══╦════╝
                                               ║
     ╔═══════════╦═══════════╦═══════════╦═════╩═════╦═══════════╦═══════════╦═══════════╗
     ║           ║           ║           ║           ║           ║           ║           ║
╔════╩═════╗╔════╩═════╗╔════╩═════╗╔════╩═════╗╔════╩═════╗╔════╩═════╗╔════╩═════╗╔════╩═════╗
║ Node 1   ║║ Node 2   ║║ Node 3   ║║ Node 4   ║║ Node 5   ║║ Node 6   ║║ Node 7   ║║ Node 8   ║
║ RPi Zero ║║ RPi Zero ║║ RPi Zero ║║ RPi Zero ║║ RPi Zero ║║ RPi Zero ║║ RPi Zero ║║ RPi Zero ║
╚══════════╝╚══════════╝╚══════════╝╚══════════╝╚══════════╝╚══════════╝╚══════════╝╚══════════╝
```

The Raspberry Pi Zero was chosen for the client nodes primarily as a factor of the cost of the boards. Currently I can only get hold of them one at a time so each one incurs its own shipping costs. Despite this, they are only costing me £6.50 per node. Comparing this to the RPi 3 Model B, which is certainly a more powerful computer, I would be paying £28.50 per node.

The argument could (quite sensibly) be made that the fact that an RPi 3 has a 4-core processor and a built-in ethernet port makes up for the fact that it costs over 4 times as much as the RPi Zero. This is almost certainly true, the RPi 3 would probably make for a much more powerful supercomputer, but the purpose of this project is not to build a very powerful supercomputer, it is to learn about building clustered supercomputers. As such, a supercomputer with 8 RPi Zero nodes is more appropriate than one with 2 RPi 3 nodes.

The server node was chosen to be an RPi 3 because I already had one lying around.

## Goals
* Make a supercomputer out of Raspberry Pis.
* Examine the runtimes of highly parallelised and single threaded programs running on the Etaerion supercomputer compared to a single Raspberry Pi.
* Set the supercomputer up to do something long term.
