# Smart-Irrigation-System



## Why?
Water and electrical energy have become very costly. Irrigation for farmers, for example, wastes massive amounts of both water and electrical energy.  irrigation systems are backbone of our  17–18% GDP of our county . And increasingly its becoming necessary for farmers to use sensors that read enviormental conditions and turn on the water only when needed so as to prevent under watering or over watering  which wastes water as well as electricity.

## How?
an automated micro-irrigation system is a device that allows one to deliver water to plants more efficiently and reduce the use of energy by up to 80%. The SBC [single board computing] can be built out of readily available materials (with no moving parts) which makes it qualify as a "Do-it-yourself" system. In its basic form the SBC costs approximately ₹1000-₹3500 to build making it affordable for everyone who maintains a small plant collection at home or a large farmland.




```bash

                 ┌───────web-server────────┐
  ┌───────┐      │                         │
  │ input ├───┬──┼────┐  ┌────────┐        │
  └───────┘   │  │    └──► get_ev │        │                   ┌──────────────┐
              │  │       └───┬────┘ ┌──────┼───────────────────┤    Relay     │
┌─────────────┤  │           │      │      │                   ├──────────────┤
│ open-weather│  │       ┌───┴────┐ │      │                   │┼┼┼┼┼┼┼┼┼┼┼┼┼┼│
│     api     │  │       │get_time├─┘      │                   ├──────────────┤
└─────────────┘  │       └────────┘        ├───────────────────┤              │
                 │                         │                   │ rassberry-pi │
                 └─────────────────────────┘                   │              │
                                                               └──────────────┘


```

![](Assets/arch-diagram.png)

<br>
<br>
<br>

![hehe](https://memeies.herokuapp.com/farming)

## Setup

### Using setup.sh
```bash
git clone https://github.com/anomius/mitwpu-hack.git
cd mitwpu-hack
nano API.py
### edit the following line to the end of the file
### owm = pyowm.OWM('Enter OWM api token')
chmod +x setup.sh
./setup.sh
```

```
python -m venv IOT
source IOT/bin/activate
pip install -r requirements.txt
```

