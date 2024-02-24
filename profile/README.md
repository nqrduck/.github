 # NQRduck
 
![](https://github.com/nqrduck/.github/blob/main/profile/images/Logo_full.png)
 
This program is intended as a educational tool for magnetic resonance experiments (NMR, NQR, ...). Its focus lies on modular behaviour depending on what nqrduck modules are installed. The core of the program is the [nqrduck](https://github.com/nqrduck/nqrduck). It provides a central interface for communication between the different modules. The nqrduck core loads all the installed modules in your python environment.

The focus for spectrometers currently lies on LimeSDR based spectrometers (LimeSDR USB, LimeSDR Mini 2.0).

## Installation 
Installation instructions can be found in the [nqrduck](https://github.com/nqrduck/nqrduck) repository. Different modules can be installed to your liking and depending on what functionality you need. 

## [NQRduck](https://github.com/nqrduck/nqrduck)
The nqrduck module is the core application. It loads all the installed modules in your python environment. It also provides a central interface for communication between modules. 

## Modules

### [nqrduck-spectrometer](https://github.com/nqrduck/nqrduck-spectrometer)
The spectrometer module provides a unified interface for different modules to communicate with spectrometers. The actual spectrometers are then implemented as submodules of this spectrometer module.

### [nqrduck-spectrometer-limenqr](https://github.com/nqrduck/nqrduck-spectrometer-limenqr)
The  LimeNQR module is a submodule of the [spectrometer module](https://github.com/nqrduck/nqrduck-spectrometer). It uses the LimeSDR based spectrometer. It provides a Graphical User Interface (GUI) for the control of the LimeSDR based spectrometer. The module uses the LimeDriver project for the control of the LimeSDR based spectrometer [1]. 

### [nqrduck-spectrometer-simulator](https://github.com/nqrduck/nqrduck-spectrometer-simulator)
The Simulator module is a submodule of the [spectrometer module](https://github.com/nqrduck/nqrduck-spectrometer).The Simulator module is used to simulate magnetic resonance experiments. It is based on the bloch simulator by C. Graf [2].

### [nqrduck-pulseprogrammer](https://github.com/nqrduck/nqrduck-pulseprogrammer)
The pulseprogrammer module is used to create pulse sequences with a user interface for magnetic resonance  experiments.


### [nqrduck-autotm](https://github.com/nqrduck/nqrduck-autotm)
The autotm module is used for automatic tuning and matching of the spectrometer. It  uses the hardware design and software from the [ATM](https://github.com/nqrduck/ATM). It can also be used to perform S11 measurements probe coils.

### [nqrduck-measurement](https://github.com/nqrduck/nqrduck-measurement)
The measurement module is used to perform single frequency measurements with the spectrometer. It also provides signal processing for the measurements.

### [nqrduck-broadband](https://github.com/nqrduck/nqrduck-bradband)
The broadband module is used to perform broadband measurements with the spectrometer.

### [nqrduck-module](https://github.com/nqrduck/nqrduck-module)
This module is a template for the creation of new modules. It provides a basic structure for the creation of new modules.


## Other Projects

### [nqr-blochsimulator](https://github.com/nqrduck/nqr-blochsimulator)
This repository contains the Bloch simulator for the NQRduck project. It is based on the simulation of Bloch equations using symmetric operator splitting by C. Graf [2].

### [LimeDriver](https://github.com/nqrduck/limedriver)
The LimeDriver project is used to control the LimeSDR based spectrometer. It is used by the LimeNQR module. The original code for the control of the LimeSDR based spectrometer was part of the paper by A. Doll [1].


### [LimeDriverBindings](https://github.com/nqrduck/LimeDriverBindings)
This repository contains the python bindings for the LimeDriver project. It is used by the NQRduck LimeNQR module.


### [ATM](https://github.com/nqrduck/ATM)
This repository contains the hardware design and software for the automatic tuning and matching (ATM) unit. 


### [LimeNQR](https:github.com/nqrduck/LimenNQR)
This repository contains the hardware design for the LimeSDR based spectrometer. 


## References
[1] [A. Doll; Pulsed and continuous-wave magnetic resonance spectroscopy using a low-cost software-defined radio. AIP Advances 1 November 2019; 9 (11): 115110. https://doi.org/10.1063/1.5127746](https://doi.org/10.1063/1.5127746)

[2] [C. Graf, A. Rund, C.S. Aigner, R. Stollberger, Accuracy and Performance Analysis for Bloch and Bloch-McConnell simulation methods Journal of Magnetic Resonance 329(3):107011 doi: 10.1016/j.jmr.2021.107011](https://doi.org/10.1016/j.jmr.2021.107011)

## Contributing
If you're interested in contributing to the project, start by checking out our [nqrduck-module template](https://github.com/nqrduck/nqrduck-module). To contribute to existing modules, please first open an issue in the respective module repository to discuss your ideas or report bugs.

## License
Modules are generally licensed under the MIT License, and hardware projects are under the CERN Open Hardware License. For specifics, please refer to the license file in each individual repository.

## FAQ
- Why is the project called NQRduck?
  - The project was initially developed for NQR (Nuclear Quadrupole Resonance) experiments. The 'duck' part is just because ducks are very cool 🦆. This project was totally not actually developed by a duck doing NQR experiments.

- Can I use the project for pulsed NMR (Nuclear Magnetic Resonance) experiments?
  - Yes, the project is designed to be used for NMR experiments as well. It was also tested with NMR experiments. 

- What future spectrometers are planned to be supported?
  - A RedPitaya based  spectrometer is planned to be supported in the future.

- What future modules are planned? (I'm primarily writing down some ideas here)
    - A module for management of different samples (T1, T2 library ...). 
    - A module for magnet spoiling.
    - A module for temperature control of the experiments.
    - Future ideas are always welcome; please share them as issues in the main repository!

- Is this also useful for research?
  - Yes, especially the Bloch simulation could be used for easy preparation of experiments because of the graphical interface for pulse sequence design. Additionally the open source nature of the project allows for easy integration of self-built hard- and software.

## Notes
This project originated as a Master's thesis at Graz University of Technology and has since evolved. The original thesis can be accessed [here](https://github.com/nqrduck/Thesis), but note that it might not reflect the current state of the project. Releases of the project that coincide with the thesis submission are tagged as "Masterproject" for reference.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
--> 
