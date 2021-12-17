# linux-clicky

This is an application to make your keyboard make sounds if your keyboard doesn't make sounds or if you want sounds to go with your keyboard sounds.  

Python3 version of linux-clicky. Lemme' know if it works out for you. This should not require root access, but I am still testing it.  

```
# Installation
sudo apt install sox python3 
git clone
cd linux-clicky
./main.py

Inspired by colszowka's [linux-typewritter](https://github.com/colszowka/linux-typewriter) script, linux-clicky produces a sound everytime you press a key on your keyboard. This might be useful for screensharing or a screencast if you want to have some type of feedback while you type.

## Usage

Run the main.py file and it will automaticly detect your keyboards and start *clickytty click*.

**Because of the way the script detects the keypresses (by tying itself to the event file in Linux, just like a keylogger would do) it requires root access**

If you are worried about malicious code, the script is pretty small you can easily read it in five minutes, so feel free to.

## Advantages over the original script:

- Entirely written in Python;
- Supports basic volume control;
- Uses threads to avoid problems with quick typing;
- Produces the sound on key down, this way the sound doesn't loop if you keep the key pressed.
- It's possible to diversify the sound of some keys. By default the SPACE and ENTER key have a specific sound. In the future, if more soundbanks are added, more special sounds for specific keys can also be easily added.

## Disadvantages

- Requires root access # Not sure if this is still the case, but it is not required for me.
- It was coded while I was taking a break from another project, so expect a bit of bad code here and there (feel free to submit patches and report bugs).

## Dependencies

- Linux (tested under Ubuntu 12.04)
- Python (tested under 2.7.3)
- SoX (in debian based systems install by typing "sudo apt-get install sox");

## Future

This is a very simple script therefore it's probably not gonna have a lot of focus on development, but I would love to add some more soundbanks into it, especially from mechanical keyboards. If you are interested in providing some  recordings feel free to contact me.

Also since this is such a small script, please be aware that it may take me a while to get around to reply to bug reports.

## License

The code is under the supplied MIT license, therefore it's completely open source.

evdev.py (by Micah Dowty <micah@navi.cx>) is included under the terms of the GPLv2. Thanks to Micah Dowty for writing this module since without it this script would not be possible, or at least not as easy to code.

The keyboard sounds were extracted from ['keyboard-typing’ by Anton](http://www.freesound.org/samplesViewSingle.php?id=137) at Freesound
