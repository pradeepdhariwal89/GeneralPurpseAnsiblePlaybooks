# Ansible Playbook Repository

This repository contains a collection of Ansible playbooks designed for general system setup and configuration. The playbooks are organized into separate folders, each focused on a specific task or service.

## Repository Structure

The repository is structured as follows:

Each folder represents a distinct task or service (e.g., "fedora41-config", "neovim-setup", "k8s-fedora41").  The files within each folder are designed to work together to achieve the task's goals.

Each folder must contain below three files.

*   `ansible.cfg`:  Global Ansible configuration file.
*   `inventory`:  Contains the inventory file used to define the target hosts.
*   `playbook.yaml`:  The main Ansible playbook file for the task.

## Supported Tasks

Here's a breakdown of the available tasks and their intended purpose:

*   **`fedora41-config`:**  Update and install essentials to fresh fedora install.
    *   **Description:** This playbook configures the new install of fedora server with essential applications and latest updates.
    
*   **`neovim-setup`:**  Install neovim with kickstart config. 
    *   **Description:** This playbook installs specific or latest neovim and configure it with kickstart, most used neovim configuration.
    
*   **`k8s-fedora41`:** Install Kubernetes cluster on fedora 41 server.
    *   **Description:**  This playbook installs and configures a specific version of Kubernetes on Fedora 41.

## Prerequisites

*   **Ansible Installation:** You must have Ansible installed on your control machine.

    **Easy Ansible Installation Instructions:**

    1.  **Install Dependencies:** Ensure you have Python and Python pip installed.

    2.  **Install Ansible:**  Use pip to install Ansible:

        ```bash
        pip install ansible
        ```

    3.  **Verify Installation:**  Check the Ansible version:

        ```bash
        ansible --version
        ```

## Usage Instructions

1.  **Clone the Repository:** Clone the repository to your local machine:

    ```bash
    git clone git@github.com:pradeepdhariwal89/GeneralPurpseAnsiblePlaybooks.git
    cd GeneralPurpseAnsiblePlaybooks
    ```

2.  **Configure Inventory:** The `inventory` file defines the target hosts where Ansible will execute the playbooks.  Modify this file to include the IP addresses or hostnames of your servers.

3.  **Update playbook variables:** The `playbook.yaml` contains essential variables with default values, modify these to reflect values relevant to your environment.

4.  **Run the Playbook:** Execute the playbook using the following command:

    ```bash
    ansible-playbook playbook.yaml
    ```

## Configuration Files

*   **`ansible.cfg`:**  This file contains global Ansible configuration settings.  You can modify it to customize settings such as the default inventory location, the SSH username, and the verbosity of the output.

## Contributing

Contributions to this repository are welcome!  Please submit pull requests with well-documented changes.
