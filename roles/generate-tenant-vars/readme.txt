This role will be executed across all the hosts listed in $PWD/inventory/{{site}}/hosts.yml

This role will generate variables required to generate tenant config for all leaf and spine devices 

Input file for this role is:-
- $PWD/inventory/lab/group_vars/all/tenants.yaml

Output file generate by this role is:
- $PWD/host_vars/{{site}}/{{inventory_hostname}}/generated-tenant-vars.yaml

In output file following list of items will be generated:-
- INFRA_NW:  Will be used to generate config for infrastructure networks  or SRIOV networks . Each infra_nw can be created either in CRB or ERB mode
- OVERLAY_NW: will be used to generate config for IP-VPN (Contrail VN) extended to SDN-Gateway


This role will accept north interfaces configured in 2 ways in the 'group_vars/all/tenants.yaml' file, it is possible to have 
a mix of both styles:

1) This results in the same IP address added in interfaces & BGP sessions upstream on the spines 
north_if:
  - vlan_id: 2002
    local_ip: 10.255.1.0/31 
    peer_ip: 10.255.1.1/31
    local_as: 12345
    peer_as: 54321

2) This results in a different IP address on each spine
north_if:
  - vlan_id: 2002
    phy_if:
      - local_ip: 10.255.1.0/31 
        peer_ip: 10.255.1.1/31
        local_as: 12345
        peer_as: 54321
        parent: spine_01
      - local_ip: 10.255.123.0/31      
        peer_ip: 10.255.123.1/31
        local_as: 12345
        peer_as: 54321
        parent: spine_02

