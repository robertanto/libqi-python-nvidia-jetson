# libqi-python-nvidia-jetson

Compiled qi library for interfacing with Pepper and Nao robots using python on Jetson Nano, Tx2, Xavier.


![](https://img.shields.io/badge/build-arm64-green.svg)
![](https://img.shields.io/badge/python-2.7-green.svg)
![](https://img.shields.io/badge/jetson-Nano-blue.svg)
![](https://img.shields.io/badge/jetson-TX2-blue.svg)
![](https://img.shields.io/badge/jetson-Xavier-blue.svg)

## Requirements

- python 2.7
- JetPack >= 3.3.1

To install the library:

```bash
git clone https://github.com/robertanto/libqi-python-nvidia-jetson.git
cd libqi-python-nvidia-jetson
chmod u+x install.sh
./install.sh
```

## Usage

```python
import qi

# Connect to the robot
session = qi.Session()
session.connect("tcp://127.0.0.1:9559") # Robot IP

# TextToSpeech service
tts = session.service("ALTextToSpeech")
tts.say("Hi, the library works!")

session.close()
```

## Acknowledgements

This library has been compiled starting from the following codes:

- libqi: [https://github.com/aldebaran/libqi](https://github.com/aldebaran/libqi) 
- libqi-python: [https://github.com/aldebaran/libqi-python](https://github.com/aldebaran/libqi-python) 
