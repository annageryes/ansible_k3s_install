# ansible_k3s_install  - HW4
Written by anna sakran 
August 2024 - devops course
Task requirments is defined in [task.md](task.md)

### requirments:
  - server node with ansible to run the playbook on 
  - one or more node VM with ansible ( MUST PROVIDE IN  [hosts.txt](hosts.txt) node names with the user if you will not be using the class nodes we practiced)
### how to run:
  run the bash script to trigger the playbook:
  ```./run_playbook ``` 

  the script will ask for two passwords:
  - the BECOME password : provide you sudo password
  - SSH password:  provide the password to connect to the nodes

### Solution Sturcture Explained:
 #### main playbook:
    The main playbook id devided into two sections:

     1-  copies the needed files to the server and installs k3s once locally
     2-  the second part runs on the remote vms and installs K3S agent on each one

 #### roles:
     - copy:     copies the executables and binaries from the playbook to their defualt route (as specified in install.sh)
                 (this role contains the RPM and install files in roles/copy/files)
     - install:  installs K3S on te master (locally) using the install script (https://docs.k3s.io/installation/airgap)
                 saves the server URL and agent token in registers
     - agent:    installs the K3S on the nodes with the Server URL and agent-token
                 * the inventory fle has the vm nodes name I used with defaults credintial - make sure to adjust for your specific needs
                
