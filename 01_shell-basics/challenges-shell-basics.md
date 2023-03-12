# Challenges: Shell Basics

## Visual Studio Code Setup

> 💡 Following these steps you will install some basic extensions for Visual Studio Code and do some
> required setup for the course.

1. Open **Visual Studio Code**
2. Open the Extensions Panel (<kbd>⇧</kbd><kbd>⌘</kbd><kbd>X</kbd>)
3. Install the following extensions
   - [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
   - [Live Preview](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server)
   - [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
   - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
4. Open the Visual Studio Code settings (<kbd>⌘</kbd><kbd>,</kbd>)
   - Search for "Default Formatter" and set to "Prettier - Code formatter"
   - Search for "Format On Save" and check the checkbox
   - > 💡 This will set up Visual Studio Code to automatically format your code on save using
     > Prettier.
5. Allow opening VS Code with the `code` command from the terminal:

- On Mac and Linux:
  - Open the command palette by pressing <kbd>⇧</kbd><kbd>⌘</kbd><kbd>P</kbd>.
    - Type "shell command" into the prompt.
    - Select _"Shell Command: Install 'code' command in PATH"_ and confirm the installation by
      pressing <kbd>Enter</kbd>.
    - > 💡 This allows you to open a folder in Visual Studio Code from the command line with the
      > `code .` command.
- On Windows with git bash terminal:
  - find out where your VS Code is installed on your machine. We need the path where the `Code.exe` actually is. The path could probably look something like this `/c/Users/YOUR_USER_NAME/AppData/Local/Programs/Microsoft\ VS\ Code`
    - important is to add a backslashes before spaces and to use only forward slashes otherwise
    - Your Code.exe of VS Code might be in a different path. Please adjust accordingly
    - Save the path into your clipboard
  - go to your home directory with
    ```
    cd $HOME
    ```
  - create a `.bash_profile` file with
    ```
    touch .bash_profile
    ```
  - add the following information to the newly created `.bash_profile` file where the git bash can find the VS Code program:
    ```
    export PATH=/c/Users/YOUR_USER_NAME/AppData/Local/Programs/Microsoft\ VS\ Code:$PATH
    ```
    - use the path that you actually have in your clipboard

## Treasure Hunt

Open **iTerm** and navigate to the folder you want to use for all your projects (create it if
nessesary). Use the following command to download the challenge files:

> 💡 This command will ask you for permission to download ghcd. This is a tool that we use to
> download challenges from GitHub to your computer. Press <kbd>Enter</kbd> to confirm the download.

```
npx ghcd@latest spicedacademy/fs-web-exercises/tree/main/sessions/shell-basics/treasure-hunt
```

Once the download is complete, navigate into the `treasure-hunt` folder using the `cd` command. Now
the real challenge begins.

**Find the lost diamond of the ancient monarch of treasure island!** Navigate through treasure
island only with the terminal and find the treasure.

Use the following commands:

- `cd` to change directories
- `cd ..` to move up one folder
- `ls` to list files the current folder
- `cat <filename>` to see contents of a file
- `pwd` to see your current directory path

Good luck! 💎

## Notes Project

Create the following file structure in a new folder inside your projects folder (using `mkdir`,
`touch` and `cd`):

```
notes
├── released
│   └── public
│   │   └── trash.txt
│   ├── announcement1.txt
│   └── announcement2.txt
└── unreleased
    ├── announcement3.txt
    └── private
        ├── notes1.txt
        └── notes2.txt
```

Update the structure to the following (using `mv`, `rm` and `cd`):

```
notes
├── private
│   ├── notes1.txt
│   └── notes2.txt
└── public
    ├── released
    │   ├── announcement1.txt
    │   └── announcement2.txt
    └── unreleased
        └── announcement3.txt
```

> 💡 You can use the `tree` command to see the file structure in the terminal. The `tree` command
> line tool was installed with the `web-setup` script.