[![Build status](https://ci.appveyor.com/api/projects/status/abxwkv2tfxcnoepc?svg=true)](https://ci.appveyor.com/project/davidt0x/pybmt)

# Python Ball Motion Tracking (**pybmt**)

Python Ball Motion Tracking (`pymbt`) is a python interface for running Richard J. Moore's [FicTrac](https://github.com/rjdmoore/fictrac) in a closed-loop manner - it facilitates behavioral and neural recording experiments that involve head-fixed flies walking on a spherical treadmill (ball), and uses the motion of the ball to modulate various outputs (e.g., the delivery of stimuli). **pybmt** allows researchers to easilly run **FicTrac** from a python program and allow ball tracking information to be processed in real time for closed-loop experiments. Since **pybmt** is not a replacement for FicTrac, the user is expected to be experienced with configuring and calibrating FicTrac. This code handles all the details of spawning, managing, and communicating the state of FicTrac, using a simple python based API. It is a useful tool for researchers wishing to build their closed-loop experiments in python.

## Getting Started

These instructions will get **pybmt** running on your local machine for development and testing purposes. 

### Prerequisites

**pybmt** requires Python 3.6+ and a working version of **FicTrac** to be present on the system. __IMPORTANT!__ Currently, the only supported version of **FicTrac** is [our forked version](https://github.com/murthylab/fictrac/tree/control_features) of **FicTrac Version 2.0**. Check the [releases page](https://github.com/murthylab/fictrac/releases/tag/v2.0.2) for pre-built binaries for your system. We hope to have these changes merged into the upstream [FicTrac GitHub repo](https://github.com/rjdmoore/fictrac) soon. 

Below are instructions for installing our version of **FicTrac** on your system.

### Windows

Download our custom pre-built version of **FicTrac** [here](https://github.com/murthylab/fictrac/releases/download/v2.0.2/fictrac_v2.0.2_control_features_x64_windows.zip). Extract the archive and add the resultant folder to your system path. 

### Linux

Coming soon ...

### Installing **pybmt**

To install **pybmt**:

```
git clone https://github.com/murthylab/pybmt.git
cd pybmt
pip install .
```

To run a quick demo:

```
cd example
python run_example.py
```

## Example Experiment

To implement your own closed-loop experiment logic take a look and `run_example.py` and `pybmt/callback/threshold_callback.py`. The basic idea is that you need to create a new class that inherits from `pybmt.callback.P 

## Built With

* [FicTrac](https://github.com/rjdmoore/fictrac) - **FicTrac** provides all the tracking!
* [ZeroMQ](http://www.zeromq.org/) - Low-latency cross platform messaging  

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/murthylab/pybmt/tags). 

## Authors

* **David Turner** and **David Deutsch** - __Murthy Lab__, __Princeton Neuroscience Institute__, and __Princeton University__ 

See also the list of [contributors](https://github.com/murthylab/pybmt/contributors) to the code.

## License

This project is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License - see the [LICENSE](LICENSE) file for details.

## Research

If you use **pybmt** and **FicTrac** as part of your research, please acknowledge David Turner, David Deutsch, and Mala Murthy (Princeton Neuroscience Institute), and also cite the original FicTrac publication:

> RJD Moore, GJ Taylor, AC Paulk, T Pearson, B van Swinderen, MV Srinivasan (2014). *"FicTrac: a visual method for tracking spherical motion and generating fictive animal paths"*, Journal of Neuroscience Methods, Volume 225, 30th March 2014, Pages 106-119. [[J. Neuroscience Methods link]](https://doi.org/10.1016/j.jneumeth.2014.01.010) [[Preprint (pdf) link]](https://www.dropbox.com/s/sw6qcmphk417bgi/2014-Moore_etal-JNM_preprint-FicTrac.pdf?dl=0)

## Acknowledgments

* **Richard Moore** - author of **FicTrac**
