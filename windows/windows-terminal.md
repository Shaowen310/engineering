# Windows Terminal

## Settings

```json
// To view the default settings, hold "alt" while clicking on the "Settings" button.
// For documentation on these settings, see: https://aka.ms/terminal-documentation
{
    "$schema": "https://aka.ms/terminal-profiles-schema",
    "defaultProfile": "{adc1f953-8a62-41e7-a273-42f71f639fdb}",
    "profiles": [
        {
            "guid": "{adc1f953-8a62-41e7-a273-42f71f639fdb}",
            "hidden": false,
            "name": "Anaconda",
            "commandline": "powershell.exe -ExecutionPolicy ByPass -NoExit -Command & 'C:\\Users\\example\\AppData\\Local\\Continuum\\anaconda3\\shell\\condabin\\conda-hook.ps1' ; conda activate 'C:\\Users\\example\\AppData\\Local\\Continuum\\anaconda3'; cd ~ "
        },
        {
            "guid": "{c6eaf9f4-32a7-5fdc-b5cf-066e8a4b1e40}",
            "hidden": false,
            "name": "Ubuntu-18.04",
            "source": "Windows.Terminal.Wsl",
            "colorScheme": "Dracula",
            "fontFace": "Ubuntu Mono derivative Powerline"
        },
        {
            // Make changes here to the powershell.exe profile
            "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
            "name": "Windows PowerShell",
            "commandline": "powershell.exe",
            "hidden": false
        },
        {
            // Make changes here to the cmd.exe profile
            "guid": "{0caa0dad-35be-5f56-a8ff-afceeeaa6101}",
            "name": "cmd",
            "commandline": "cmd.exe",
            "hidden": false
        },
        {
            "guid": "{574e775e-4f2a-5b96-ac1e-a2962a402336}",
            "hidden": false,
            "name": "PowerShell Core",
            "source": "Windows.Terminal.PowershellCore"
        },
        {
            "guid": "{b453ae62-4e3d-5e58-b989-0a998ec441b8}",
            "hidden": false,
            "name": "Azure Cloud Shell",
            "source": "Windows.Terminal.Azure"
        }
    ],
    // Add custom color schemes to this array
    "schemes": [
        {
            "name": "flat-ui-v1",
            "background": "#000000",
            "black": "#000000",
            "blue": "#2980b9",
            "brightBlack": "#7f8c8d",
            "brightBlue": "#3498db",
            "brightCyan": "#1abc9c",
            "brightGreen": "#2ecc71",
            "brightPurple": "#9b59b6",
            "brightRed": "#e74c3c",
            "brightWhite": "#ecf0f1",
            "brightYellow": "#f1c40f",
            "cyan": "#16a085",
            "foreground": "#ecf0f1",
            "green": "#27ae60",
            "purple": "#8e44ad",
            "red": "#c0392b",
            "white": "#ecf0f1",
            "yellow": "#f39c12"
        },
        {
            "name": "Dracula",
            "background": "#282A36",
            "black": "#21222C",
            "blue": "#F1FA8C",
            "brightBlack": "#6272A4",
            "brightBlue": "#D6ACFF",
            "brightCyan": "#A4FFFF",
            "brightGreen": "#69FF94",
            "brightPurple": "#FF92DF",
            "brightRed": "#FF6E6E",
            "brightWhite": "#FFFFFF",
            "brightYellow": "#FFFFA5",
            "cyan": "#8BE9FD",
            "foreground": "#F8F8F2",
            "green": "#50FA7B",
            "purple": "#BD93F9",
            "red": "#FF5555",
            "white": "#F8F8F2",
            "yellow": "#F1FA8C"
        }
    ],
    // Add any keybinding overrides to this array.
    // To unbind a default keybinding, set the command to "unbound"
    "keybindings": []
}
```