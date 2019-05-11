# ansible-inventory
A repo to study ansible static and dynamic inventories

Example test:

ansible -i ./dynhosts ansible-node01.carcano.local -m debug -a "var=hostvars[inventory_hostname]"

outpus should be something like

ansible-node01.carcano.local | SUCCESS => {
    "hostvars[inventory_hostname]": {
        "ansible_check_mode": false, 
        "ansible_playbook_python": "/usr/bin/python2", 
        "ansible_version": {
            "full": "2.3.1.0", 
            "major": 2, 
            "minor": 3, 
            "revision": 1, 
            "string": "2.3.1.0"
        }, 
        "company": "Carcano.SA", 
        "dns": "ns1.carcano.local,ns2.carcano.local", 
        "group_names": [
            "ch", 
            "site1"
        ], 
        "groups": {
            "all": [
                "manager-node01.carcano.local", 
                "ansible-node01.carcano.local", 
                "ansible-node02.carcano.local"
            ], 
            "ch": [
                "ansible-node01.carcano.local", 
                "ansible-node02.carcano.local"
            ], 
            "site1": [
                "ansible-node01.carcano.local", 
                "ansible-node02.carcano.local"
            ], 
            "ungrouped": [
                "manager-node01.carcano.local"
            ]
        }, 
        "inventory_dir": "/home/student/ex407/0000-solutions/inventory", 
        "inventory_file": "/home/student/ex407/0000-solutions/inventory/dynhosts", 
        "inventory_hostname": "ansible-node01.carcano.local", 
        "inventory_hostname_short": "ansible-node01", 
        "ntp": "ntp.ch.carcano.local", 
        "omit": "__omit_place_holder__484918257374c8b5bfc87312eb8227b21f047f04", 
        "playbook_dir": ".", 
        "role": "balancer"
    }
}

