# Client Steps
## Add Server for monitoring
1. Edit servers file add server you want monitoring 
2. Add hosts to Prometheus Server ( cause we use monitoring by server hostname )
3. Auto Add ssh hostkey
```bash
ansible-playbook -i servers ssh-hostkey-checking.yaml
```
4. Install Node Exporter ( both centos & ubuntu )
```bash
ansible-playbook -i servers install-node-exporter.yaml
```
#
# Server Setup & Config
## Install prometheus stack
```bash
ansible-playbook -i servers install-prometheus-stack.yaml
```

## Reload prometheus configuration
Edit config files in `conf` folder, and run:
```bash
ansible-playbook -i servers reload-prometheus-config.yaml
```

## Install Exporters on VM instances
Node exporter:
```bash
ansible-playbook -i servers install-node-exporter.yaml
```
##
