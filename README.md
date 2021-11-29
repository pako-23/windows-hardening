# windows-hardening
This repository contains the Windows 10 hardening baseline script for the OS
hardening course.
The configurations applied by the script are based on
[the following framework](https://github.com/microsoft/SecCon-Framework/blob/master/level-1-enterprise-basic-security.md).

# Set up
Before running the Ansible playbook from the Ansible server, the provisioned
machines should first run the script `.\provision.ps1` to set up WinRM.
The steps implemented in the script are based on the Ansible
[documentation](https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#winrm-setup).
Then, on the Ansible server the dependencies required to run Ansible can be run
by using the command `pip3 install -r requirements.txt`.

# Audit
For the audit part of the assignment, it is sufficient running the command
`ansible-playbook -C assignment.yml`. The command runs the playbook without
applying any change to the provisioned machine, so it shows the changes that
Ansible would make and how the machine does not comply with the baseline
into the playbook.
