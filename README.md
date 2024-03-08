# Acid Analyzer

The most accurate open source spectrum analyzer. Check out this video to see what I'm talking about.
https://www.youtube.com/watch?v=xpjekAgWM44

The analyzer works well on systems that use Pipewire audio by default.
These include Debian 12 and above, Ubuntu 22.10 and above and Arch Linux (if you choose Pipewire audio when installing).
I tried adding support for PulseAudio and ALSA but got frustrated by their interfaces. Pipewire audio is much more robust and sensible.
I found out that Debian 12 XFCE doesn't install Pipewire audio by default even though the Gnome version does. Perhaps there is more variability inside other distros too. Let me know if your distro is one of those.

The spectrum is drawn in the terminal using ncurses or a window using GLFW. I will make a proper mouse controlled graphical interface in the future. Now you'll have to control it via the command line arguments.

I'll make a Windows version at some point. I find porting and compiling to Windows to be quite difficult. It's not as developer friendly as Linux. If you are good at this please contact me. Any help is welcome.


## Installation

```console
sudo apt install libfftw3-bin ncurses-bin libglfw3
git clone https://github.com/yliniemi/AcidAnalyzer
AcidAnalyzer/AcidAnalyzer/build/AcidAnalyzer
```


## Compilation

### Prerequisites for Debian 12 and above

```console
sudo apt install cmake pkg-config libpipewire-0.3-dev libfftw3-dev libncurses-dev libglfw3-dev
```


### Actual compilation

```console
git clone https://github.com/yliniemi/AcidAnalyzer
git clone https://github.com/glfw/glfw
git clone https://github.com/KdotJPG/OpenSimplex2
cd AcidAnalyzer/AcidAnalyzer/build/
cmake ..
make
./AcidAnalyzer
```


## Interfacing

### Command line arguments

Example
```console
./AcidAnalyzer --fps 122 --FFTsize 16384 --dynamicRange 60 --kaiserBeta 5.0 --glfw false --ncurses true
```

### Keyboard shortcuts

You can close the program either by pressing ESC or Q
M toggles the visibility of the mouse
F toggles the full screen
B toggles the borderless window



