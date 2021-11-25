# windows-hardening
To run it first run the `provision.ps1` script on the Windows 10 machine
to set up the services needed by ansible.
Then, you can set up the required packages on the Ansible server by running
`pip3 install -r requirements.txt`.
To audit the Windows machine you can run `ansible-playbook -C assignment.yml`
which will tell you if there are any changes needed to have the machine
complying with the baseline developed.
To apply the baseline run `ansible-playbook assignment.yml`.
