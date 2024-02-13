
# Installing and Running Conda via Bash

This guide provides instructions on how to install Miniconda on Linux and set up a basic Conda environment. Miniconda is a minimal installer for Conda, which is an open-source package management system and environment management system that runs on Windows, macOS, and Linux.

## Prerequisites

- You should have `wget` installed on your Linux system.
- You should have `bash` or `zsh` as your shell.

## Installation Steps

1. **Create a Directory for Miniconda3**

   Create a new directory where Miniconda will be installed.

   ```bash
   mkdir -p ~/miniconda3
   ```

2. **Download the Miniconda Installer Script**

   Use `wget` to download the latest version of Miniconda for Linux.

   ```bash
   wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
   ```

3. **Run the Installer Script**

   Execute the installer script with the following command. The flags used are:
   - `-b`: run install in batch mode (without manual intervention),
   - `-u`: update an existing installation,
   - `-p`: specify installation path.

   ```bash
   bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
   ```

4. **Clean Up the Installer Script**

   After the installation is complete, you can remove the installer script.

   ```bash
   rm -rf ~/miniconda3/miniconda.sh
   ```

5. **Initialize Conda for Your Shell**

   Initialize Conda for `bash` and `zsh` to make Conda commands available in your terminal.

   ```bash
   ~/miniconda3/bin/conda init bash
   ~/miniconda3/bin/conda init zsh
   ```

   Close and reopen your terminal after this step for the changes to take effect.

## Creating and Activating a Conda Environment

1. **Create a New Conda Environment**

   You can create a new Conda environment named `btenv` (or any other name you prefer) with the following command:

   ```bash
   conda create -n btenv
   ```

2. **Activate the New Environment**

   Activate the newly created Conda environment with:

   ```bash
   conda activate btenv
   ```

   You should now see `(btenv)` or the name of your environment before the command prompt, indicating that the environment is active.

## Final Notes

You should have now installed Miniconda and created a new Conda environment. You can start installing packages and working within this environment.

For more detailed information on using Conda, refer to the [official Conda documentation](https://docs.conda.io/projects/conda/en/latest/).

