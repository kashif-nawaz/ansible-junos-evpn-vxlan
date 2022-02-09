This role will be executed across all the hosts listed in $PWD/inventory/{{site}}/hosts.yml

This role will check if required VLANs have been configured in the leaf and spine devices or not

Input file for this role is:-

- {{playbook_dir}}/host_vars/{{site}}/{{inventory_hostname}}/generated-overlay.yaml

Output of this role will be displayed in the terminal from where playbook is executed
