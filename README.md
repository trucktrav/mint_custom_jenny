install ansible 
sudo pacman -S ansible

# Update package list first
sudo apt update

# Install Ansible
sudo apt install ansible

# Install git if not already present (should be from your playbook)
sudo apt install git

# Install python3-pip for additional modules if needed
sudo apt install python3-pip


# Install collections from requirements.yml
ansible-galaxy install -r requirements.yml

# Or specifically for collections:
ansible-galaxy collection install -r requirements.yml

# Run the playbook
ansible-playbook playbook.yml

# Or with verbose output to see what's happening:
ansible-playbook -v playbook.yml

# Or if you need to become root for certain tasks:
ansible-playbook --ask-become-pass playbook.yml