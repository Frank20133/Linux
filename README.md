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
//Head of the file
Name=Eclipse
//Name of the application, also the name shows when the mouse moves onto.
Type=Application
//Classification
Exec=/opt/eclipse/eclipse
//Real execution, it must be correctly point to the file `.exe`
Terminal=false
//Using the terminal?
Icon=/opt/eclipse/icon.xpm
//Figure of the shortcut
Comment=Integrated Development Ecvironment
//Description of the file
NoDisplay=false
//Hide the list?
Categories=IDE;
//Where the list should belong to
```
- 3. Save the file and you can drag the shortcut from `applications` to taskbar.
- 4. Saving the file `.desktop` may fail. `sudo chmod 777 eclipse.desktop` before saving will help.

How to set environmental variables
----
    First to go to `/etc` then `sudo gedit profile`, then type environmental variables before saving. `source /etc/profile` 
    in terminal at the end. 
Take JDK as an example:
- 1. First to go to `/etc` then `sudo gedit profile`
- 2. Type the following at the end:
```JAVA
    export JAVA_HOME=/usr/share/jdk1.6.0_14 
    export PATH=$JAVA_HOME/bin:$PATH 
    export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar 
```
- 3. `source /etc/profile` after saving.
Notice：
- 1. Change `/usr/share/jdk1.6.0_14` to your own JDK installation location.
- 2. Using `:` to separate path.
- 3. `$PATH / $CLASSPATH / $JAVA_HOME` is a kind of way to refer to the original environmental variables. It is a common-seen mistake
to cover the original values when setting new values without reference.
- 4. The current directory `.` in the head of `CLASSPATH` should not be missed.
- 5. `export` exports these three variables to be the global variables.
- 6. Case sensitive.
