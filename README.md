# How to Open VS Code from the Terminal on macOS

This guide explains how to open Visual Studio Code from the terminal on a Mac using a custom command.

### Prerequisites

- **macOS** operating system.
- **Visual Studio Code** installed on your machine.

### Steps

1. **Open the Terminal**
   - Press `Cmd + Space`, type `Terminal`, and press `Enter` to open the terminal.

2. **Add the Custom Command**
   - To enable opening VS Code from the terminal, we’ll define a custom function. This function can be added to your shell configuration file.

   - For **bash** (older macOS versions), open `.bash_profile`:
     ```bash
     nano ~/.bash_profile
     ```

   - For **zsh** (default shell in newer macOS versions), open `.zshrc`:
     ```bash
     nano ~/.zshrc
     ```

3. **Define the Custom Function**
   - Add the following function at the end of the file:
   
     ```bash
     code () {
       VSCODE_CWD="$PWD" open -n -b "com.microsoft.VSCode" --args $* ;
     }
     ```
   - This function allows you to open Visual Studio Code with a specific file or folder from the terminal.

4. **Save and Apply Changes**
   - Save the file by pressing `Ctrl + O` and then `Enter`.
   - Exit the editor by pressing `Ctrl + X`.
   - To apply the changes, run the following command:
     ```bash
     source ~/.bash_profile  # or source ~/.zshrc for zsh
     ```

5. **Test the Command**
   - To open a file or directory in VS Code, use the following command:
     ```bash
     code namefile
     ```
   - Replace `namefile` with the name of the file or directory you wish to open.

### Conclusion

You have now successfully set up a command to open Visual Studio Code directly from the terminal on your macOS. This will make it quicker and easier to launch your editor without having to manually open it.

Feel free to customize or extend the command as needed. Enjoy coding with VS Code!
