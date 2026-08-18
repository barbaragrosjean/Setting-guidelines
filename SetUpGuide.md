# Setup Guide to Work with VS Code on hyades00

## 1. Set up VS Code Compatibility

### 1.1 Download 
Download a compatible version (1.85.2) of VS Code for the server.  
Link here: [Visual Studio Code Version 1.85.2][link_to_VSCODE]

[link_to_VSCODE]: https://code.visualstudio.com/updates/v1_85 "Visual Studio Code version 1.85.2"

Select the option suited for your computer:  
> Downloads: Windows: x64 Arm64 | Mac: Universal Intel Silicon | Linux: deb rpm tarball Arm snap

### 1.2 Download Extensions 

Go to the extensions button on the left of the window (or press ⇧ + ⌘ + X (Mac)).

Search for and install the following extensions:
- Remote - SSH
- Remote - SSH Editing 
- Remote Development
- Remote Explorer
- Jupyter
- VS Code Jupyter Notebook 

## 2. Connect to the Server
- Go to the bottom-left button: `Open a Remote Window`
- Select `Connect to Host...`
- `Add New SSH Host`
- Enter the SSH key: `ssh your_user_name_stormdb@hyades01.pet.auh.dk`
- Enter your password for StormDB

**Config File:**  
- Go to the bottom-left button `Open a Remote Window`
- Select `Connect to Host...`
- Select the config file (should be something ending with `/.ssh/config`)
- Add the following to the file:  
    > Host hyades01.pet.auh.dk  
    > HostName hyades01.pet.auh.dk  
    > User *your_user_name*  

## 3. Environment Setup 
Open a terminal: Go to the top bar, select `Terminal`, then `New Terminal`.

### 3.1 Miniconda
In the terminal, run:  
- `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`  
This will download the file from the internet. If it fails on the server terminal, install it locally and copy-paste the file to the server.

- `bash Miniconda3-latest-Linux-x86_64.sh`

### 3.2 Create Environment and Install Libraries
**Create an environment:**  
Terminal: `conda create -n name_of_your_new_env`

**Activate the environment:**  
Terminal: `conda activate name_of_your_new_env`

**Install libraries:**  
Terminal: `conda install name_of_the_library`  

*NOTE:* Sometimes the installation channel for Conda is required. Check the library’s documentation page if mentioned.

### 3.3 Use the Environment
#### 3.3.1 On Terminal 
To run anything using this environment, go to the top bar, select `Terminal`, then `New Terminal`.

Activate the environment:  
Terminal: `conda activate name_of_your_environment`

Once done, you can run a Python file (.py). Make sure you are in the folder containing your file; otherwise, provide the full path:  
Terminal: `python name_of_your_file.py`

#### 3.3.2 On Notebook
When running for the first time, it will ask you to select a kernel. You should see your environment in the list provided. If not, check the VS Code Jupyter Notebook extension or close and reopen VS Code if you just installed it.  
To change the environment after one is already set by default, click on your environment name at the top right of the page; it will prompt you to choose an environment again.





