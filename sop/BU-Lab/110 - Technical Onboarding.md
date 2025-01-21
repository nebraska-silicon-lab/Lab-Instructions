# Lab:110 - Technical Onboarding

Last Updated: July 6, 2023

This SOP consists of a list of resources that contain information helpful for getting up to speed with the technical aspects of work in the Detector Lab. It is broken down into three parts: Information helpful for working with the equipment and software in the lab, information on the CMS detector, and resources for the specific subdetectors that the detector lab is working on.

## Working in the Lab

  - The [lablog](nebraskadetectorlab.com) is an important resource for working in the lab. It primarily offers a message board-like interface for documenting work and reporting issues. It also has sections for creating requisitions for needed purchases and a listing of equipment in the lab that includes links to datasheets and manuals. 
  - We operate a test stand for QA of the TFPX modules that are produced in the lab. Instructions on how to operate the test stand are available [here](). TODO: Find resource
  - In the cleanroom we use a robotic gantry for module assembly. In-person training is required to operate the gantry, but the resources [here](https://github.com/CUASAS/pixel-gantry-control) and [here](https://drive.google.com/drive/folders/1jjhutLgPGgwVizSZdoIk1yHqYb2zJ_WL) are good to review prior to training.
  - 

### Programming Resources

Basic programming skills are indispensable when performing analysis or debugging software in the lab. Broadly speaking, the relevant knowledge areas for lab work are programming languages, operating systems, and version control.

#### Programming Languages

**Python**

In our lab, the single most important programming language to be familiar with is Python. It is used broadly in the development of test software as well as when performing data analysis (physics or otherwise). If you have previous imperative programming experience (C, C++, Java, etc) a good jumpstart is available [here](https://learnxinyminutes.com/docs/python/), however if you are starting from zero then the resources [here](https://docs.python.org/3/tutorial/) will be more appropriate. In addition to the core python language there are a few libraries that are used extensively in our work.

  - [matplotlib](https://matplotlib.org/) is the standard for data visualization in Python. With it, you can quickly create many of the basic kinds of plots that you are familiar with: line graphs, scatter plots, histograms, and so on. It also gives you extensive customization to mix different types of plots to create your own data visualization. To get a feel for what matplotlib is capable of, check out the [gallery](https://matplotlib.org/stable/gallery/index).
  - [numpy](https://numpy.org/) is a library for doing high speed numeric calculations with Python. It essentially consists of a menu of pre-compiled low-level routines that allow you to crunch numbers at speeds normally only achievable in compiled languages like C. It also provides an expressive programming interface which allows you to write down complicated data manipulations with only a few lines of code.
  - [uproot](https://uproot.readthedocs.io/en/latest/basic.html) is a library for interacting with ROOT files in pure python. As is mentioned in the C++ section, ROOT is the ubiquitous data analysis framework in particle physics. Traditionally analyists will write their routines in C++ utilizing functions provided by ROOT, but increasingly analysts prefer to implement their routines in Python utilizing the libraries mentioned above. `uproot` allows you to read and write the same ROOT files as the traditional C++ workflow, but from Python and without needed ROOT installed locally.
  - [scikit-hep](https://scikit-hep.org/) is a collection of useful packages for performing more complicated data analysis. Useful for finding tools in the python ecosystem that are replacements for the tools provided by ROOT.

When developing Python locally, the [Pycharm](https://www.jetbrains.com/pycharm/) IDE is recommended which includes useful features like auto-completion, an builtin visual debugger, version control integration, as well as many others. The community edition is available for free, but you can also apply for an educational license of the professional edition.


**C++**

The C++ language is a compiled, multi-paradigm (although primary object oriented) language that has been historically, and in many places is still currently, the de-facto language for data processing and analysis software in particle physics. The most popular analysis framework used in particle physics is [ROOT](https://root.cern.ch/) and it is a C++ framework.

TODO: Add links to resources.

**LabVIEW**

LabVIEW is a piece of software developed by National Instruments that is used primarily for hardware control and monitoring. The labview software is controlled by a visual language called "G", but this language is often referred to itself as LabVIEW. The main use of LabVIEW in the lab for implementing the gScript interpreter that is responsible for controlling the gantry.

UNL has a site license for labview. During installation, point the installer to `ni-license.unl.edu`. It may say that it fails to get the license, but this seems to just be a UI bug. You can then proceed with using the software regardless. 

**gScript**

`gScript` is a domain-specific language (DSL) for operating the gantry system in the cleanroom. It is a simple BASIC-like language that executes commands one at a time from top to bottom. The main [gScript documentation](https://github.com/CUASAS/pixel-gantry-control/blob/master/Gantry/gScript%20Application/gScript%20Documentation.md) explains the language in more detail, and some [example scripts](https://github.com/CUASAS/pixel-gantry-control/tree/master/Example%20Project/Scripts) are available as well.

#### Operating Systems

TODO: Identify relevant resources for the below (eg bash stuff for linux, getting a windows install through the electronics shop and so on)

**Linux**

**Windows**

**Mac**


#### Version Control

Version control 

TODO: Find git resources

## The CMS Detector

 


## Subdetectors

### TFPX, the Tracker Forward PiXel Detector

TODO: Fill in the links below

  - [Technical Design Review](https://cds.cern.ch/record/2272264/files/CMS-TDR-014.pdf)
  - Mattermost Channel
  - CMS Talk Channel
  - Twiki

### ETL, the Endcap Timing Layer

  - [Technical Design Review](http://cds.cern.ch/record/2667167/files/CMS-TDR-020.pdf?version=2)

