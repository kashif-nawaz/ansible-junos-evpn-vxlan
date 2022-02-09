This role will be executed across all the hosts listed in $PWD/inventory/{{site}}/hosts.yml

This role will check status of VTEP interfaces 

Input file for this role is:-

- {{playbook_dir}}/host_vars/{{site}}/{{inventory_hostname}}/generated-overlay.yaml

Output of this role will be displayed in the terminal from where playbook is executed
