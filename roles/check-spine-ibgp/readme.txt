This role be executed across all the spine devices listed in $PWD/inventory/{{site}}/hosts.yml

This role will verify if spine to spine and spine-contrail MP-iBGP sessions are in  establish state or not

Input files for this role are:-

- {{playbook_dir}}/host_vars/{{site}}/{{inventory_hostname}}/generated-overlay.yaml

Output will be displayed in the terminal from where playbook is executed 
