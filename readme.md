
# Godot C# Template (Blank)

A simple template setup to create a C# based project for Godot 4.x.

This project provides basic configuration for [Visual Studio Code](https://code.visualstudio.com/) and Visual Studio to run and debug Godot projects using C#.

## Godot Location

The main thing required to make debugging work for Visual Studio is the location of the Godot IDE executable. The instructions below are provided for Windows users. Alternatively, you can replace the quoted `program` value with your executable path in the `.vscode/launch.json` file.

For convenience and shareability, it is assumed you've created an environment variable named `GODOT4` that points to the full path and filename of the executable. e.g.

    C:\Godot>SET GODOT4
    GODOT4=C:\Godot\Godot_v4.1.1-stable_mono_win64.exe

You can set this using the Settings app in Windows:

1. Search for "environment"
2. Select "Edit the system environment variables"
3. Click on the "Environment Variables..." button
4. Click on the "New..." button for either a User or System variable
5. Provide a variable name of `GODOT4`
6. Provide a variable value of the full path, executable name, and extension to Godot for your system, e.g. C:\Godot\Godot_v4.1.1-stable_mono_win64.exe
7. Click the OK button for the "New User Variable" dialog
8. Click the OK button for the "Environment Variables" dialog
9. Restart VS Code if it's running.

**Note:** If you close the "Environment Variables" dialog instead of clicking the "OK" button, the environment variables may not be updated until your machine restarts. If you find the value hasn't taken, you can re-edit the value in the dialog, and click OK again both times, then restart VS Code.

## Using this Template

To use this template to start a new project:

    dotnet new install Mikeware.Godotnet.BlankTemplate

Navigate to the parent folder where you'd like to install your project:

    dotnet new godotcsharp -n YourProjectNameHere

You can then use the `Import` button in the Godot Project Manager to select this folder.

To select VS Code as your default editor, go to Editor->Editor Settings... in the Godot Menu. Scroll down to the Dotnet->Editor item in the left-hand tree, then select your desired External Editor from the dropdown. No other changes should be required.

Visual Studio can also be used, though console output will not display, to receive Godot error messages, you must turn on native debugging in the Launch settings by right-clicking on the project, going to Properties, and then the Debug tab. See more information about working with Visual Studio [from the Godot Plugin repository here](https://github.com/godotengine/godot-csharp-visualstudio/issues/48).

## Notes on this Template

This template provides the bare minimum of a File->New Godot project with C# debugging support added on.

It was created and tested on Windows 10 with Godot 4.1.

If you're looking for a more advanced template with extra features, I suggest looking at [Chickensoft's Game Template](https://github.com/chickensoft-games/GodotGame).

If this template has helped you, please let us and other folks know, thanks!

## Godot 3.x

_This should work for Godot 3.x as well, though is untested; modify the `.vscode/settings.json` and remove the `godot_tools.gdscript_lsp_server_port` entry._

## License

This project template is provided as-is for you to use for any of your projects under a CC0 license.

**Note:** The `icon.svg` file is licensed by Creative Commons Attribution 4.0 International, [see here](https://godotengine.org/press/), [license text](https://creativecommons.org/licenses/by/4.0/). No changes were made.

For more information about Godot's Engine license and code created with Godot, [see here](https://godotengine.org/license/)
