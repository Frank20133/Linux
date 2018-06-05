# Simple use of Linux
How to change password of root
----
- Input `sudo passwd` in shell, first input your password, then type new password. After trying it many times, 
the original password fo root mostly is root.

How to create shortcut: take eclipse as an example
----
- 1. Create and edit shortcut file: `sudo gedit /usr/share/applications/eclipse.desktop`
- 2. Type the following content in the file
```Java
[Desktop Entry]
Name=Eclipse
Type=Application
Exec=/opt/eclipse/eclipse
Terminal=false
Icon=/opt/eclipse/icon.xpm
Comment=Integrated Development Ecvironment
NoDisplay=false
Categories=IDE;
