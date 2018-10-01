## LINUX Visual Studio Code empty example & openFrameworks

OpenFrameworks empty example working on Visual Studio Code IDE.
- Linux POP! OS 18.04 or Ubuntu 18.04 LTS ( GCC-7 , G++-7 )
- openFrameworks 0.10.0 gcc6
- Microsoft Visual Studio Code IDE 1.27.2 for Linux Ubuntu

![Image](/imgs/1.png)

# Example project

 * Copy and paste /openFrameworks_VisualStudioCode_Example into /apps/myApp
 * Rename your project folder as you wish
 * Rename openFrameworks_VisualStudioCode_Example.code-workspace with the same project name
 * Open the folder with Visual Studio Code 
 * In c_cpp_properties.json rename your OF workspace folder
 * In launch.json change your app name 
 
```
   "linux": {
                "MIMode": "gdb",
                "setupCommands": [
                    {
                        "description": "Enable pretty-printing for gdb",
                        "text": "-enable-pretty-printing",
                        "ignoreFailures": true
                    }
                ],
                "program": "${workspaceRoot}/bin/exampleVSC"
```

 ![Image](/imgs/3.png)
 
 * In task.json you can lauch a shell bash and create your task for Build 
 
 ```
 "tasks": [
        {
            "type": "shell",
            "label": "OPENFRAMEWORKS BUILD RELEASE",
            "presentation": {
                "reveal": "always",
                "panel": "new"
            },
            "command": "make",
            "args": [
                "-j4"
            ],
 ```
 * Addons : simply add your oF addons in addons.make file
 
 * Run Build Task with CTRL + SHIFT + B 
 
 * Install the extension adds language support for C/C++ to Visual Studio Code and C++ Intellisense fo gcc-x86

![Image](/imgs/3.png)

* run 'make RunRelease' from visual studio code 
 
 


 


