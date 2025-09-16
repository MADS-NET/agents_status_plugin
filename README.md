# agents plugin for MADS

This is a Sink plugin for [MADS](https://github.com/MADS-NET/MADS). 

This plugin keeps track of launched agents and of their current status.

*Required MADS version: 1.3.5.*


## Supported platforms

Currently, the supported platforms are:

* **Linux** 
* **MacOS**
* **Windows**


## Installation

Linux and MacOS:

```bash
cmake -Bbuild -DCMAKE_INSTALL_PREFIX="$(mads -p)"
cmake --build build -j4
sudo cmake --install build
```

Windows:

```powershell
cmake -Bbuild -DCMAKE_INSTALL_PREFIX="$(mads -p)"
cmake --build build --config Release
cmake --install build --config Release
```


## INI settings

The plugin supports the following **mandatory** settings in the INI file:

```ini
[agents_status]
silent = true
sub_topic = ["agent_event"]
```


## Datastore
The plugin supports a datastore file `agents.json` created in a temporary directory for persisting data between runs. Look at the `Datastore` class for more information on how to use it.



## Executable demo

<Explain what happens if the test executable is run>

---