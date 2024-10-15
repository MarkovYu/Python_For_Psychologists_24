# Setup for the course

There are a few things you need to get working on your machine in order to follow this course. However, don't worry as it's all gonna be [open source](), won't require a lot of storage and will be explained in detail.

```{note}
Importantly, some of the content on this page is outdated because it uses more complex environments like Git, etc. In the 2024 version of the course, we will focus more on Python itself rather than IDE environments. So, don't stress too much about all this information—just focus on the 2024 section.
```

## General things 2024

There are a few computing requirements for the course that are absolutely necessary (beyond the few software packages you should install, described below):

- **Laptop** You must have administrator access to your computer (i.e., you must be able to install things yourself without requesting IT approval).
- **Operating Systems**: Windows, macOS, or Linux
- **Python version**: Anaconda comes with its own Python installation, so no need to pre-install Python
- **Disk Space**: At least 3 GB of free disk space for the base installation
- **Internet Access**: Required for downloading the installer


If you foresee any of these being a problem please reach out to one of the instructors and enquire what steps you can take to ensure your setup is ready for the course.

## Required software 2024

To get the most out of the course, we ask that you arrive with the following software already installed:

- [`Discord`](https://discord.com/) (for communication purposes)
- A `modern web-browser`
- `Python 3` via [`Anaconda`](https://docs.conda.io/projects/conda/en/latest/index.html)
- `PsychoPy` (https://www.psychopy.org/) (we will need much later)


The rest of this page provides more detail on installation procedures for each of the above elements, with separate instructions for each of the three major operating systems (`Windows`, `Mac OS`, and `Linux`).

## Discord 2024

Go to https://discord.com/ and download and install Discord. Please note, that you can also use Discord through your browser if you don't want to download it. This will be the main channel of communication for the course.

## Modern web browser 2024

Install Firefox or Chrome.
(Safari will also work.)

## Anaconda Installation with Jupyter Notebook 2024
## Installation Instructions

````{tab-set}
```{tab-item} Windows Installation

### Step 1: Download Anaconda
- Go to the [Anaconda website](https://www.anaconda.com/products/distribution).
- Click on the "Download" button and choose the Windows version that matches your system architecture (64-bit recommended).

### Step 2: Run the Installer
- Locate the downloaded `.exe` installer and double-click it to run.
- Click "Next" and accept the default installation settings.
- Choose whether to install Anaconda for "Just Me" or "All Users." For most cases, "Just Me" is sufficient.
- **Important**: You will be prompted to add Anaconda to your system’s `PATH`. It is recommended **not** to check this option. Anaconda will manage the environment for you.

### Step 3: Complete the Installation
- Once installed, open the "Anaconda Navigator" from the Start Menu or search for it.

### Step 4: Launch Jupyter Notebook
- In Anaconda Navigator, locate "Jupyter Notebook" and click "Launch." This will open Jupyter Notebook in your browser.
```

```{tab-item} macOS Installation

### Step 1: Download Anaconda
- Go to the [Anaconda website](https://www.anaconda.com/products/distribution) and download the macOS installer.

### Step 2: Install Anaconda
- Open the downloaded `.pkg` file and follow the on-screen instructions.
- During the installation, the installer will ask you to install Anaconda for "Just Me" or "All Users." You can choose based on your needs.

### Step 3: Update the Terminal Profile (optional)
- If you want to use `conda` in the terminal, ensure Anaconda is added to your shell's startup file.
  - For **bash** users, this is typically in `.bash_profile`.
  - For **zsh** users, it’s in `.zshrc`.

- You can do this by adding the following line to the respective file:
  bash
  export PATH="/Users/your-username/anaconda3/bin:$PATH"
  

### Step 4: Launch Jupyter Notebook
- Open the terminal and type:
  bash
  jupyter notebook
  
- Jupyter Notebook will open in your default browser.
```

```{tab-item} Linux Installation

### Step 1: Download Anaconda
- Head over to the [Anaconda website](https://www.anaconda.com/products/distribution) and download the Linux installer (64-bit `.sh` file).

### Step 2: Install Anaconda
- Open the terminal and navigate to the directory where the installer was downloaded.
- Run the following command to start the installation:
  bash
  bash Anaconda3-2024.XX-Linux-x86_64.sh
  
  Replace `2024.XX` with the version number you downloaded.

- Follow the prompts to complete the installation. You’ll be asked to approve the license terms and specify the installation path.

### Step 3: Update Shell Profile
- After installation, you may need to update your shell’s startup file (e.g., `.bashrc` or `.zshrc`) to add Anaconda to your `PATH`.
  bash
  export PATH="~/anaconda3/bin:$PATH"
  

### Step 4: Launch Jupyter Notebook
- In your terminal, run:
  bash
  jupyter notebook

- This will open Jupyter Notebook in your browser.
```
````

## Verifying Your Installation 2024

To ensure Anaconda and Jupyter Notebook were installed correctly, you can run the following commands in your terminal or Anaconda Prompt:

bash
conda --version

This should display the installed version of Conda.

bash
jupyter notebook

This should launch Jupyter Notebook in your web browser.

## Conclusion 2024

Now that you've successfully installed Anaconda, you can easily manage your Python environments and use Jupyter Notebook for interactive coding. Anaconda simplifies package management and deployment, making it a great choice for both beginners and experienced users.

## Required software (Legacy, pre 2024)

To get the most out of the course, we ask that you arrive with the following software already installed (software/things in () are not entirely necessary but definitely great to have):

- A command-line shell: [`Bash`](https://www.gnu.org/software/bash/)
- (A version control system: [`Git`](https://git-scm.com/))
- A remote-capable text editor: [`VSCode`](https://code.visualstudio.com/)
- `Python 3` via [`Miniconda`](https://docs.conda.io/en/latest/miniconda.html)
- (A [`GitHub`](https://github.com/) account)
- [`Discord`](https://discord.com/) (for communication purposes)
- A `modern web-browser`

If you already have all of the above software tools/packages installed (what are you even doing here?), or are confident you’ll be able to install them by the time the course starts, you can jump straight to [checking your install](#checking-your-install).
The rest of this page provides more detail on installation procedures for each of the above elements, with separate instructions for each of the three major operating systems (`Windows`, `Mac OS`, and `Linux`).

### Some quick general notes on instructions

- There is no difference between `Enter` and `Return` in these instructions, so just press whatever the equivalent on your keyboard is whenever one is stated
- If you already have some of these things installed on your computer already that should (theoretically) be okay.
  However, you need to make sure that you are able to complete the steps described in [checking your install](#checking-your-install) without issue.
  - For example, having multiple different `Python` installations on your computer can lead to incredibly frustrating issues that are very difficult to debug.
    As such, if you have already installed `Python` via some other application (not `Miniconda`/`Anaconda`), it's strongly encouraged to uninstall it before following the instructions below.
    You _must_ have `Python` installed via `Miniconda` for this course.

### OS-specific installation instructions

Select the tab that corresponds to your operating system and follow the instructions therein.

````{tab-set}
```{tab-item} Windows
**Windows Subsystem for Linux (WSL)**

1. Search for `Windows Powershell` in your applications; right click and select `Run as administrator`.
   Select `Yes` on the prompt that appears asking if you want to allow the app to make changes to your device.
2. Type the following into the Powershell and then press `Enter`:

        Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

3. Press `Enter` again when prompted to reboot your computer.
4. Once your computer has rebooted, open the Microsoft Store and search for "Ubuntu."
   Install the program labelled "Ubuntu 18.04" (not "Ubuntu 16.04" or "Ubuntu") by clicking the tile, pressing `Get`, and then `Install`.
5. Search for and open Ubuntu from your applications.
   There will be a slight delay (of a few minutes) while it finishes installing.
6. You will be prompted to `Enter new UNIX username`.
   You can use any combination of alphanumeric characters here for your username, but a good choice is `<first_initial><last_name>` (e.g., `jsmith` for John Smith).
   You will then be prompted to enter a new password.
   (Choose something easy to remember as you will find yourself using it frequently.)
7. Right click on the top bar of the Ubuntu application and select "Properties".
   Under the "Options" tab, under the "Edit Options" heading, make sure the box reading "Use Ctrl+Shift+C/V as Copy/Paste" is checked.
   Under the "Terminal" tab, under the "Cursor Shape" heading, make sure the box reading "Vertical Bar" is checked.
   Press "Okay" to save these settings and then exit the application.

(The above step-by-step WSL instructions are distilled from [here](https://docs.microsoft.com/en-us/windows/wsl/install-win10) and [here](https://docs.microsoft.com/en-us/windows/wsl/initialize-distro).
If you have questions during the installation procedure those resources may have answers!)

From this point on whenever the instructions specify to "open a terminal" please assume you are supposed to open the Ubuntu application.

**Bash shell**

You already have it, now that you’ve installed the WSL!

**Git**

You already have it, now that you’ve installed the WSL!

**VSCode**

1. Go to https://code.visualstudio.com/ and click the download button, then run the `.exe` file.
1. Leave all the defaults during the installation with the following exception:
      - Please make sure the box labelled "Register Code as an editor for supported file types" is selected

**VSCode extensions**

1. Open the Ubuntu application.
1. Type `code .` into the terminal and press `Enter`.
   You should see a message reading "Installing VS Code Server" and then a new windows will open up.
1. Press `Ctrl+Shift+P` in the new window that opens and type "Extensions: Install extensions" into the search bar that appears at the top of the screen.
   Select the appropriate entry from the dropdown menu that appears (there should be four entries; simply select the one that reads "Extensions: Install extensions").
1. A new panel should appear on the left-hand side of the screen with a search bar.
   Search for each of the following extensions and press `Install` for the first entry that appears. (The author listed for all of these extensions should be "Microsoft".)
      - Python (n.b., you will need to reload VSCode after installing this)
      - Live Share (n.b., you may need to press "Ctrl/Cmd+Shift+P" and type "install extensions" again after installing this)
      - Live Share Extension Pack
      - Docker
      - Remote - WSL

**Python**

1. Open a new terminal and type the following lines (separately) into the terminal, pressing `Enter` after each one:

        wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
        bash Miniconda3-latest-Linux-x86_64.sh

1. A license agreement will be displayed and the bottom of the terminal will read `--More--`.
   Press `Enter` or the space bar until you are prompted with "Do you accept the license terms? [yes|no]."
   Type `yes` and then press `Enter`
1. The installation script will inform you that it is going to install into a default directory (e.g., `/home/$USER/miniconda3`).
   Leave this default and press `Enter`.
1. When you are asked "Do you wish the installer to initialize Miniconda3 by running conda init? [yes|no]," type `yes` and press `Enter`.
   Exit the terminal once the installation has finished.
1. Re-open the Ubuntu application.
   Type `which python` into the terminal and it should return a path (e.g., `/home/$USER/miniconda3/bin/python`).
   - If you do not see a path like this then please try typing `conda init`, closing your terminal, and repeating this step.
     If your issue is still not resolved skip the following step and contact an instructor on the #help-installation channel on the BHS Slack.
1. Type the following to remove the installation script that was downloaded:

        rm ./Miniconda3-latest-Linux-x86_64.sh


**Python packages**

Open a terminal and type the following commands:

        conda config --append channels conda-forge
        conda config --set channel_priority strict
        conda install -y flake8 ipython jupyter jupyterlab matplotlib numpy pandas scipy seaborn pingouin statsmodels plotly
```

```{tab-item} Linux
**Bash shell**

You already have it!
Depending on which version of Linux you’re running you may need to type `bash` inside the terminal to access it.
To check whether this is necessary, follow these steps:

1. Open a terminal and type `echo $SHELL`.
   If it reads `/bin/bash` then you are all set!
   If not, whenever the instructions read "open a terminal," please assume you are to open a terminal, type `bash`, and the proceed with the instructions as specified.

**Git**

You may already have it; try typing `sudo apt-get install git` (Ubuntu, Debian) or `sudo yum install git` (Fedora) inside the terminal.
If you are prompted to install it follow the instructions on-screen to do so.

**VSCode**

1. Go to https://code.visualstudio.com/ and click the download button for either the .deb (Ubuntu, Debian) or the .rpm (Fedora, CentOS) file.
1. Double-click the downloaded file to install VSCode.
   (You may be prompted to type your administrator password during the install).

**VSCode extensions**

1. Open the Visual Studio Code application.
1. Press `Ctrl+Shift+P` in the new window that opens and type "Extensions: Install extensions" into the search bar that appears at the top of the screen.
   Select the appropriate entry from the dropdown menu that appears (there should be four entries; simply select the one that reads "Extensions: Install extensions").
1. A new panel should appear on the left-hand side of the screen with a search bar.
   Search for each of the following extensions and press `Install` for the first entry that appears. (The author listed for all of these extensions should be "Microsoft".)
      - Python (n.b., you will need to reload VSCode after installing this)
      - Live Share (n.b., you may need to press "Ctrl/Cmd+Shift+P" and type "install extensions" again after installing this)
      - Live Share Extension Pack
      - Docker

**Python**

1. Open a new terminal and type the following lines (separately) into the terminal, pressing `Enter` after each one:

        wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
        bash Miniconda3-latest-Linux-x86_64.sh


1. A license agreement will be displayed and the bottom of the terminal will read `--More--`.
   Press `Enter` or the space bar until you are prompted with "Do you accept the license terms? [yes|no]."
   Type `yes` and then press `Enter`
1. The installation script will inform you that it is going to install into a default directory (e.g., `/home/$USER/miniconda3`).
   Leave this default and press `Enter`.
1. When you are asked "Do you wish the installer to initialize Miniconda3 by running conda init? [yes|no]," type `yes` and press `Enter`.
   Exit the terminal once the installation has finished.
1. Re-open a new terminal.
   Type `which python` into the terminal and it should return a path (e.g., `/home/$USER/miniconda3/bin/python`).
   - If you do not see a path like this then please try typing `conda init`, closing your terminal, and repeating this step.
     If your issue is still not resolved skip the following step and contact an instructor on the #help-installation channel of the BHS Slack.
1. Type the following to remove the installation script that was downloaded:

        rm ./Miniconda3-latest-Linux-x86_64.sh

**Python packages**

Open a terminal and type the following commands:

        conda config --append channels conda-forge
        conda config --set channel_priority strict
        conda install -y flake8 ipython jupyter jupyterlab matplotlib numpy pandas scipy seaborn pingouin statsmodels plotly

```

```{tab-item} MacOs
**Bash shell**

You already have it!
Depending on which version of Mac OS you’re running you may need to type `bash` inside the terminal to access it.
To check whether this is necessary, follow these steps:

1. Open a terminal and type `echo $SHELL`.
   If it reads `/bin/bash` then you are all set!

Note: If you are using Mac Catalina (10.15.X) then it is possible your default shell is NOT CORRECT.
To set the default to bash, type `chsh -s /bin/bash` in the terminal, enter your password when prompted, and then close + re-open the terminal.

**Git**

You may already have it!
Try opening a terminal and typing `git --version`.
If you do not see something like “git version X.XX.X” printed out, then follow these steps: 

1. Follow [this link](https://sourceforge.net/projects/git-osx-installer/files/git-2.23.0-intel-universal-mavericks.dmg/download?use_mirror=autoselect) to automatically download an installer.
1. Double click the downloaded file (`git-2.23.0-intel-universal-mavericks.dmg`) and then double click the `git-2.23.0-intel-universal-mavericks.pkg` icon inside the dmg that is opened.
1. Follow the on-screen instructions to install the package.

**VSCode**

1. Go to https://code.visualstudio.com/ and click the download button.
1. Unzip the downloaded file (e.g., `VSCode-darwin-stable.zip`) and moving the resulting `Visual Studio Code` file to your Applications directory.

**VSCode extensions**

1. Open the Visual Studio Code application
1. Type `Cmd+Shift+P` and then enter "Shell command: Install 'code' command in PATH" into the search bar that appears at the top of the screen.
   Select the highlighted entry.
   A notification box should appear in the bottom-right corner indicating that the command was installed successfully.
1. Type `Cmd+Shift+P` again and then enter "Extensions: Install extensions" into the search bar.
   Select the appropriate entry from the dropdown menu that appears (there should be four entries; simply select the one that reads "Extensions: Install extensions").
1. A new panel should appear on the left-hand side of the screen with a search bar.
   Search for each of the following extensions and press `Install` for the first entry that appears. (The author listed for all of these extensions should be "Microsoft".)
      - Python (n.b., you will need to reload VSCode after installing this)
      - Live Share (n.b., you may need to press "Ctrl/Cmd+Shift+P" and type "install extensions" again after installing this)
      - Live Share Extension Pack
      - Docker

**Python**

1. Open a new terminal and type the following lines (separately) into the terminal, pressing `Enter` after each one:

        curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
        bash Miniconda3-latest-MacOSX-x86_64.sh


1. A license agreement will be displayed and the bottom of the terminal will read `--More--`.
   Press `Enter` or the space bar until you are prompted with "Do you accept the license terms? [yes|no]."
   Type `yes` and then press `Enter`
1. The installation script will inform you that it is going to install into a default directory (e.g., `/home/$USER/miniconda3`).
   Leave this default and press `Enter`.
1. When you are asked "Do you wish the installer to initialize Miniconda3 by running conda init? [yes|no]," type `yes` and press `Enter`.
   Exit the terminal once the installation has finished.
1. Re-open a terminal.
   Type `which python` into the terminal and it should return a path (e.g., `/home/$USER/miniconda3/bin/python`).
   - If you do not see a path like this then please try typing `conda init`, closing your terminal, and repeating this step.
     If your issue is still not resolved skip the following step and contact an instructor on the #help-installation channel of the BHS Slack.
1. Type the following to remove the installation script that was downloaded:

        rm ./Miniconda3-latest-MacOSX-x86_64.sh


**Python packages**

Open a terminal and type the following commands:

        conda config --append channels conda-forge
        conda config --set channel_priority strict
        conda install -y flake8 ipython jupyter jupyterlab matplotlib numpy pandas scipy seaborn pingouin statsmodels plotly
```
````

**Note**: If the instructions aren't working and you have spent more than 15-20 minutes troubleshooting on your own, reach out on the #help-installation channel on the Discord channel with the exact problems you're having.
One of the instructors will try and get back to you quickly to help resolve the situation.
If they're unable to help via `Discord`, you may be directed to attend one of the installation office hours.

### GitHub account

Go to https://github.com/join/ and follow the on-screen instructions to create an account.
It is a good idea to associate this with your university e-mail (if you have one) as this will entitle you to sign up for the [GitHub Student Developer Pack](https://education.github.com/pack) which comes with some nice free bonuses.



## Checking your install

Now that you've installed everything it's time to check that everything works as expected!
Type the following into your terminal:

    bash <( curl -s https://raw.githubusercontent.com/aylinsgl/Python_For_Psychologists_23-24/master/check_install.sh)

If you installed everything correctly you should see a message informing you as such.
If any problems were detected you should receive some brief instructions on what is wrong with potential suggestions on how to remedy it.
If you followed these instructions step-by-step and cannot resolve the issue please contact one of the course instructors for more help.

Yeah, you did! Great job!



## Getting the course content

Now that you have installed the required software (or not) to follow the course, it's time to gather the respective materials.

<img src="https://upload.wikimedia.org/wikipedia/commons/e/ea/Conda_logo.svg" alt="conda logo" width="300"/>\
<sub><sup><sub><sup>https://upload.wikimedia.org/wikipedia/commons/e/ea/Conda_logo.svg</sup></sub></sup></sub>

By installing `Python` on your system (i.e. specifically `Conda`) and setting up the appropriate environment, you will be able to open all the `Jupyter Notebooks` and go through the whole content of the course locally. 

To get things up and running, please follow these steps:

1. Download the [`environment.yml`](https://raw.githubusercontent.com/aylinsgl/Python_For_Psychologists_23-24/master/environment.yml) file (e.g. with right mouse click -> Save As). Make sure that the file ends with `.yml` and not `.txt`.
2. Open up a conda terminal (or any other terminal), and create a new conda environment with the following command: `conda env create -f /path/to/file/environment.yml` - For example ``conda env create -f ~/Downloads/environment.yml`
3. Download the notebooks in this repository via [this link](https://github.com/M-earnest/Python_for_Psychologists_Winter2022/archive/refs/heads/main.zip) and unzip them to your preferred location, e.g. `Desktop/Python_for_Psychologists_Winter2022`.
4. Next, open up a `conda terminal` (or any other `terminal`), activate the `conda environment` with `conda activate pfp_2022` (or on older `conda environment` with `source activate pfp_2022` for `mac` and `linux` and `activate pfp_2022` for `windows`).
5. Finally, via the `terminal`, move to the folder where you've put all the unzipped content of this workshop, e.g. with the command `cd ~/Desktop/Python_for_Psychologists_Winter2022` and run the command `jupyter notebook`. If the `notebook server` isn't automatically opened in a new browser window, please copy-paste either the `http://127.0.0.1:8888/...` or the `http://localhost:8888/...` path into a new browser window and press `Enter`. You should now see the `jupyter notebook server` (looking like a file browser and displaying the content of the directory). 



