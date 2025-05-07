---
description: 'Estimated Setup Time: Approximately 30 minutes'
---

# 💾 Installing VerifyWise

The recommended method of installing VerifyWise is via Docker. Before proceeding with the installation, ensure the following prerequisites are met.

### Install Docker

Verify that Docker is installed on your system. You can download and install Docker from the [official Docker website](https://www.docker.com/products/docker-desktop).

### Setting up VerifyWise in Docker

Follow these steps to set up VerifyWise in Docker:

1. **Install Visual Studio Code**: Download and install [Visual Studio Code](https://code.visualstudio.com/), a popular code editor that will help you manage your project files and run commands.
2.  **Clone the GitHub repository**: Open Visual Studio Code and use the terminal to clone the VerifyWise repository. Run the following command in the terminal:

    ```bash
    git clone https://github.com/bluewave-labs/verifywise.git
    ```
3.  **Navigate to the project directory**: Once the repository is cloned, navigate to the project directory:

    ```bash
    cd verifywise
    ```
4. **Start your local Docker instance**: Make sure your Docker application is running.
5. **Open a terminal**: In Visual Studio Code, open a bash terminal within your project directory.
6.  **Run the installation script**: Make the `install.sh` script executable and then run it:

    ```bash
    chmod +x ./install.sh
    ./install.sh
    ```

### Accessing the application

Once the installation is complete, you can access the VerifyWise application by navigating to [http://localhost:8080](http://localhost:8080) in your web browser.



