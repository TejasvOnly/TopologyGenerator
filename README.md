# TopologyGenerator
A topology generator for NS3 built on [olcpixelgameengine](https://github.com/OneLoneCoder/olcPixelGameEngine) for College Project.
This program generates a code file based on user's created topology which can be compiled in NS3. This program is by no means finished or optimized, This is just a minor project.



## How to run

#### Windows
Just clone the repository and open solution in Visual Studio, Compile the code and that's it.

#### Linux
Open terminal in the same directory as the cloned repository and use

```
g++ -o outputfilename Source.cpp -lX11 -lGL -lpng -lpthread
```

You can visit [here](https://github.com/OneLoneCoder/olcPixelGameEngine/wiki) for more information on olcpixelgameengine


### How to use

This project only uses mouse inputs.

- Hold and drag middle mouse button to pan, scroll it to zoom in and out.
- Use scroll over sidebar to change current tool.
- Use Node tool and left click to place nodes.
- Left click on any node to select it.
- Almost all tools once selected can be used via right click, Tools only affect selected nodes not the one you are currently hovering over.
- Traffic, Connection requires you first select one node and right click on other.
- Traffic is generated from selected node to right clicked node.
- Close the program to generate code file named [test1.cc](/TopologyGenerator/test1.cc), this name can be changed in [Source.cpp](/TopologyGenerator/Source.cpp).


### What does generated file do
The generated code can be compiled in ns3 by placing files [this](/TopologyGenerator/test1.cc) and [this](/TopologyGenerator/MyApp.h) to scratch folder of ns3 and compiling as usual.

This project currently only supports these functionalities :-

- Creates only point to point links.
- Generates trafffic only for tcp sockets.
- All NetDeviceContainer have same datarate and delay. This can be changed in [kernel.dat](/TopologyGenerator/kernel.dat)
