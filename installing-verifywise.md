---
description: 'Estimated Setup Time: Approximately 30 minutes'
---

# 💾 Installing VerifyWise

Currently, the recommended method of installing VerifyWise is via Docker.

Prerequisites

Before proceeding with the installation, ensure the following prerequisites are met:

#### Enable Virtualization

Before installing VerifyWise, ensure that virtualization is enabled on your system. This is necessary for Docker to function correctly. Follow these general steps to enable virtualization:

1. **Restart Your Computer**: Begin by restarting your computer.
2. **Enter BIOS/UEFI Settings**: Press the key required to enter the BIOS/UEFI settings as your computer is booting up. This key varies by manufacturer but is often one of the following: `F2`, `F10`, `F12`, `Delete`, or `Esc`. Refer to your computer's manual if you're unsure.
3. **Locate Virtualization Settings**: Once in the BIOS/UEFI settings, look for the virtualization settings. These are typically found under the "Advanced," "CPU Configuration," or "Security" tabs. The exact location can vary depending on your motherboard manufacturer.
4. **Enable Virtualization**: Look for an option labeled "Intel VT-x," "Intel Virtualization Technology," "AMD-V," or similar, and set it to "Enabled."
5. **Save and Exit**: Save your changes and exit the BIOS/UEFI settings. Your computer will restart.

#### Install Docker

Verify that Docker is installed on your system. You can download and install Docker from the [official Docker website](https://www.docker.com/products/docker-desktop).

### Setting Up VerifyWise in Docker

Follow these steps to set up VerifyWise in Docker:

1. **Install Visual Studio Code**: Download and install [Visual Studio Code](https://code.visualstudio.com/), a popular code editor that will help you manage your project files and run commands.
2.  **Clone the GitHub Repository**: Open Visual Studio Code and use the terminal to clone the VerifyWise repository. Run the following command in the terminal:

    ```bash
    git clone https://github.com/bluewave-labs/verifywise.git
    ```
3.  **Navigate to the Project Directory**: Once the repository is cloned, navigate to the project directory:

    ```bash
    cd verifywise
    ```
4. **Start Your Local Docker Instance**: Make sure your Docker application is running.
5. **Open a Bash Terminal**: In Visual Studio Code, open a bash terminal within your project directory.
6.  **Run the Installation Script**: Make the `install.sh` script executable and then run it:

    ```bash
    chmod +x ./install.sh
    ./install.sh
    ```

### Accessing the Application

Once the installation is complete, you can access the VerifyWise application by navigating to [http://localhost:8080](http://localhost:8080) in your web browser.



