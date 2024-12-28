# lldb-debug-server

Archlinux package to start a debug server with systemd on port 1234.

## Use with VSCode
Install CodeLLDB extension and create a .vscode/launch.json file:

```json
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Remote launch",
            "type": "lldb",
            "request": "launch",
            "program": "${workspaceFolder}/target/debug/inputplumber", // Local path.
            "initCommands": [
                "platform select remote-linux", // For example: 'remote-linux', 'remote-macosx', 'remote-android', etc.
                "platform connect connect://192.168.1.19:1234",
                "settings set target.inherit-env false",
            ],
            "env": {
                "PATH": "/usr/local/sbin:/usr/local/bin:/var/lib/flatpak/exports/bin:/usr/lib/rustup/bin",
            }
        }
    ]
}
```

Change the IP address accordingly.
