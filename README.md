# [dotfiles-generic]
A minimal Xorg based configuration for alpine linux systems.

# Usage
The setup has to be started using 'source setup' otherwise, aliases won't work.
Running the 'startx' command will launch Mozilla Firefox at full screen.
Most aliases (scale and resize) are executable files located under the user's home directory.


## Aliases

# scale - ~/.scale
Once called, the scale alias will return the width and height of the X session's display 0.

# resize - ~/.resize
The resize alias expects a width and height value along with an application name.
The given application must be initialized using the 'DISPLAY=:0' prefix, launching it inside the X session.
The resize alias may also be given the result of the execution of the scale alias.
Examples:
- resize 1920 1080 'Mozilla Firefox'
- resize $(scale) 'Mozilla Firefox'

# fullscreen
The fullscreen alias sets an application in fullscreen.
It is effectively equivalent to 'resize $(scale)'.
Example:
- fullscreen 'Mozilla Firefox'

# addstart - ~/.addstart
Adds an application to '.xinitrc'.
The added application will launch with the X session.
