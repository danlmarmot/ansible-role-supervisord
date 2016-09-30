An Ansible role for installing Supervisord (with systemd)

### Default versions

Supervisord 3.3.1

### Testing

A Vagrant/VirtualBox environment is provided in the /examples directory.  To get started:

1. Install Vagrant, Virtualbox, and Ansible
1. Change your directory into 'examples'
1. Run 'vagrant up' to bring up the VM.

An Ubuntu 15.10 VM will be spun up and supervisord installed.
To verify:

    vagrant ssh
    sudo su -
    sup status

### Additional notes

- For Vagrant installs, dependencies are downloaded once and cached locally.
- Each role in this Ansible playbook will check the version of each application before installing, and will not re-install if the installed version is the desired version.  This speeds up reprovisioning.
- To reprovision, use the 'vagrant provision' command.
