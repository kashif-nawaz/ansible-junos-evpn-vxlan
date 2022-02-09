This role be executed across all the leaf devices listed in $PWD/inventory/{{site}}/hosts.yml

This role will verify if LACP child interfaces are in "Collecting distributing" or not

Input file for this role is:-

- {{playbook_dir}}/inventory/{{site}}/group_vars/all/evpn-if.yaml 

Output will be displayed in the terminal from where playbook is executed 
