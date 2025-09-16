# Houdini Procedural City Generator

This project is a Houdini Digital Asset (HDA) developed as the final thesis for the Master of Science in Games Engineering degree at the University of Warwick. It provides a powerful and highly controllable toolkit for artists and designers to rapidly generate custom cityscapes and island environments.

The core goal of this project is to address the "generative trilemma" by prioritizing artistic control and modularity, offering a robust alternative to purely data-driven methods for creating large-scale, production-ready urban worlds.

![程序化城市生成效果图](https://github.com/Davecodingking/PCG-city-generator/blob/main/pcg.png)
*An example of a city generated with this HDA.*

## Core Features

* **🎨 Artist-Driven Workflow**: Utilize intuitive inputs like grayscale maps, hand-drawn curves, and custom terrain geometry to precisely guide the high-level structure of the city.
* **🧩 Modular Architecture**: The system is composed of independent generators for the main layout, road networks, various building types, and vegetation, making it easy to extend and maintain.
* **🚀 Powerful Kitbash Integration**: A dedicated Kitbash Instancer allows for the seamless integration of your own high-fidelity asset libraries, dramatically enhancing visual detail and artistic expression.
* **🎮 Sim-Ready Output**: Generates clean, editable polygonal geometry optimized for direct use in production pipelines, including game engines like Unreal Engine and Unity, as well as VFX renderers.

## Getting Started

1.  Download the `.hda` file from this repository.
2.  In Houdini, install the asset via `File > Import > Houdini Digital Asset...`.
3.  In the node network, press `Tab` and search for `procedural_city_generator` to create the node.
4.  Connect your inputs (or use the default settings) and begin adjusting parameters to generate your world!

## System Modules & Inputs

The HDA ecosystem is primarily composed of the following parts:

#### Input Methods

* **Custom Map Input**: Use a grayscale image to define the island's silhouette and influence building distribution.
* **Draw Highway Curves**: Manually draw curves to define the exact path of major highways.
* **Add Hotspots**: Place points to designate city centers or areas of high density.
* **Terrain Input**: Import a custom terrain mesh to build the city upon a non-flat landscape.

#### Core Generators

* **City_generator HDA**: The main engine that processes all inputs to generate the macro layout, terrain, road network, and various data maps (e.g., zone definitions).
* **Modular Asset Generators**: A suite of specialized generators that create procedural skyscrapers, residential buildings, houses, and vegetation based on the data maps.
* **Kitbash_Instancer HDA**: Receives the data maps and your packed Kitbash assets to efficiently instance high-quality models into the correct locations.

## Dependencies

* **SideFX Houdini 20.0** or a more recent version.
