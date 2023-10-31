# Agenda

- Environment setup
- Git
- Coding style

# Environment setup

## From compile to execution

### Compile

- translate the programming language into machine code.

- The output is usually an object file (`.o` for Unix-like systems or `.obj` for Windows).

```shell
g++ -c myprogram.c -o myprogram.o
```

Popular C++ Compiler:

- g++
- Clang

### linking

If your program consists of multiple source files or uses external libraries, you need to link them together to create an executable file. The linker resolves references between different object files, links libraries, and produces an executable file.

```shell
g++ myprogram1.o myprogram2.o -o myprogram
```

### Execution

You can execute it from the terminal like this:

```shell
./yourprogram
```

## Environment setup

**For Mac:**

- Option 1: Local Dev with VS Code
- Option2: Local Dev Container with VS Code
- Option3: Remote Dev on CSIF

**For Win**

- Option 1: Local Dev on WSL2 with VS Code
- Option2: Local Dev Container with VS Code
- Option3: Remote Dev on CSIF























### Environment Isolation

**Why**

- Different projects require different setups
- Do experiments without messing up your host env
- Security for production workloads

**How**

- Separate Physical Machines
- Virtual Machines (VMs)
- Docker Containers

**Docker Containers**

- Widely adopted and loved
- Can be used in every stage of the DevOps cycle
- Lightweight compared to Virtual Machines (VMs)
- Easy to setup across different host environments
- Code Editor support (such as VS Code and NeoVim)









### Mac Option 1: Local Dev with VS Code

### Install compiler - mac

```sh
xcode-select --install
```

Check clang

```sh
clang --version
```

#### Install IDE

My choice: Vscode https://code.visualstudio.com/

#### Install extension

- C/C++
- Code Runner

#### Modify setting

Add "--std=c++11" in args in tasks.json

settings in Code Runner













### Win/Mac Option 2: Local Dev container with VS Code

#### Download and Install Docker

Note: If you are using M1/M2 chip, make sure you are downloading the docker for apple.

#### Install IDE

Vscode https://code.visualstudio.com/

#### Click and run the script on github

https://github.com/ecs36c-fq2023/hw1/tree/main

![image-20231004201052181](/Users/hongxiangzhang/Library/Application Support/typora-user-images/image-20231004201052181.png)



















### Mac/Win Option3: Remote Dev on CSIF

Follow the steps: 

https://docs.google.com/document/d/1Zu6FPeiJv2erSm4ldKM1ncPcGL9lmq3KbHWOHzYsB-E/edit#heading=h.wfuhmktnbn7u





















### Win Option 1: Local Dev on WSL2 with VS Code

https://code.visualstudio.com/docs/cpp/config-wsl#_set-up-your-linux-environment

https://learn.microsoft.com/en-us/windows/wsl/install

https://linuxconfig.org/ubuntu-22-04-on-wsl-windows-subsystem-for-linux

#### install wsl2 extension

https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl

![image-20231004202011031](/Users/hongxiangzhang/Library/Application Support/typora-user-images/image-20231004202011031.png)

#### install Windows Subsystem for Linux

```shell
wsl --install
```

#### Install IDE

Vscode https://code.visualstudio.com/

#### Install extension

- C/C++
- Code Runner

#### Modify setting

Add "--std=c++11" in args in tasks.json

settings in Code Runner

























### Debug in VS Code

- Set Breakpoints
- Inspect Values of Variables
- Inspect Values of an Array

### Compile and run c++ project













# Git

**Why**

- Change multiple files and be able to revert to any previously *committed* state with one click/command
- Different people work on different features at the same time using different *branches*

**How**

- Using Command-line
- Using VS Code
- Using GitHub Desktop

## install and config

1. Install from the official Git website (https://git-scm.com/).
2. Configure your name and email, which will be associated with your commits.
3. set up ssh with GitHub 

## git clone \<repository URL>

- Create a copy of a remote Git repository on your local machine.
- It downloads the entire project, including its history and files, and sets up a connection to the remote repository.

## git commit -m 'Your comment'

- save changes made to your project's code into the Git repository.
- After making changes to your files, you first use `git add` to stage the changes, and then `git commit` to create a commit.
- A commit includes a message that describes the changes made in that commit, helping you and others understand the purpose of the changes.

## git push

- Upload your local Git commits to a remote repository.
- It's typically used to share your changes with others or to update a central repository.

## git pull

- Fetch changes from a remote repository and merge them into your current branch.

# Coding style

https://google.github.io/styleguide/cppguide.html
