This role be executed across all the hosts listed in $PWD/inventory/{{site}}/hosts.yml

This role will verify if eBGP between spine and leaf switches are in establish state

Input files for this role are:-

- {{playbook_dir}}/host_vars/{{site}}/{{inventory_hostname}}/generated-underlay-vars.yaml

Output will be displayed in the terminal from where playbook is executed 
