# Server Monitoring

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
