This role will be executed across all the hosts listed in $PWD/inventory/{{site}}/hosts.yml

This role will check will check "admin/config" and operational status of IP Fabric links

Input file for this role is:-

- {{playbook_dir}}/host_vars/{{site}}/{{inventory_hostname}}/generated-underlay-vars.yaml

Output of this role will be displayed in the terminal from where playbook is executed
