To do sync HA to use command: 
```
ansible-playbook -i bigips.ini backup-ucs-sync.yml -e "device_group=<HA Device Group Name> bigip_password=<Your Admin Password>" --tags sync
```

For example to run sync HA with sync tag:
    `ansible-playbook -i bigips.ini backup-ucs-sync.yml -e "device_group=device-group-failover-61000ec7fa69 bigip_password=Shengping" --tags sync`

To do configuration backup: 

```
ansible-playbook -i bigips.ini backup-ucs-sync.yml -t backup
```

Optionally, setting bigip password via adding `-e bigip_password=<your admin password>`.

For example: `ansible-playbook -i bigips.ini backup-ucs-sync.yml -t backup -e bigip_password=admin_password`