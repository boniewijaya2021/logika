# logika
# install extensions c++

# install extensions c++
# install extensions c++ extensions pack
# install extensions c++ Runner

# running project menggunakan vs code 
# g++ -std=c++17 -o main tugasbagian1.cpp && ./main

# running project menggunakan vs code 
# g++ -std=c++17 -o main tugasbagian2.cpp && ./main

#buat file task.json di dalam .vscode <br>
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "build",
            "type": "shell",
            "command": "/usr/bin/g++",  
            "args": [
                "-g",
                "${file}",
                "-o",
                "${fileDirname}/${fileBasenameNoExtension}"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "problemMatcher": ["$gcc"],
            "detail": "Generated task by Debugger."
        }
    ]
}

#edit launch.json <br>
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "(lldb) Launch",
      "type": "cppdbg",
      "request": "launch",
      "program": "enter program name, for example ${workspaceFolder}/a.out",
      "args": [],
      "stopAtEntry": false,
      "cwd": "${fileDirname}",
      "environment": [],
      "externalConsole": false,
      "MIMode": "lldb"
    },
    {
      "name": "(gdb) Launch",
      "type": "cppdbg",
      "request": "launch",
      "program": "${fileDirname}/${fileBasenameNoExtension}",
      "args": [],
      "stopAtEntry": false,
      "cwd": "${workspaceFolder}",
      "environment": [],
      "externalConsole": false,
      "MIMode": "gdb",
      "preLaunchTask": "build",
      "miDebuggerPath": "/usr/bin/gdb",
      "setupCommands": [
        {
          "description": "Enable pretty-printing for gdb",
          "text": "-enable-pretty-printing",
          "ignoreFailures": true
        }
      ],
      "logging": {
        "trace": true,
        "traceResponse": true,
        "engineLogging": true
      }
    },
    {
      "name": "C/C++ Runner: Debug Session",
      "type": "lldb",
      "request": "launch",
      "args": [],
      "cwd": "/Users/bonie/Documents/budiluhur/materi1",
      "program": "/Users/bonie/Documents/budiluhur/materi1/build/Debug/outDebug"
    }
  ]
}

