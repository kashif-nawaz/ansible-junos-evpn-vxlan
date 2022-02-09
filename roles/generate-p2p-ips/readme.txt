This role will be executed across all the hosts listed in $PWD/inventory/{{site}}/hosts.yml

This role will generate P2P IPs which will be used to further generate interfaces config 

Input file for this role is:-
- $PWD/inventory/{{site}}/group_vars/all/p2p_ips.yaml

Output file for this role is 
-$PWD/inventory/{{site}}/group_vars/all/generated_p2p_ips.yaml 


