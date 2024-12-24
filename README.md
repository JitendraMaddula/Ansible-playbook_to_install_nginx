# Ansible-playbook_to_install_nginx

This project automates the installation and setup of NGINX on a Unix-based EC2 instance using Ansible. It was created using `ansible-galaxy playbook` for a modular and reusable structure.

## Features
- Installs NGINX on a ubuntu EC2 instance.
- Starts and enables the NGINX service.
- Uses Ansible inventory file to manage the instance's configuration.

## Prerequisites
1. **Ansible**: Ensure Ansible is installed on your control machine.
   - Install Ansible: [Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
2. **Access to the EC2 instance**:
   - A valid `.pem` key file for SSH access to the EC2 instance.
   - The EC2 instance must have a public IP address and an accessible private key.

## Getting Started
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/JitendraMaddula/Ansible-playbook_to_install_nginx.git
   cd Ansible-playbook_to_install_nginx.git

2. Update the Inventory File:
    Open the inventory file and add:
    The private IP address of your EC2 instance.
    The absolute path to your .pem file.
    Example:
      [nginx_servers]
      ENTER YOUR IP ansible_user=ubuntu ansible_ssh_private_key_file=/ENTER/YOUR/PATH/FILE_NAME.pem

3. Run the Playbook:
    ansible-playbook -i inventory.ini site.yml

## Contributions

Contributions are welcome! Feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
