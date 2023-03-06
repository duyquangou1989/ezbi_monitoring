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

MySQL exporter:
```bash
ansible-playbook -i servers install-mysql-exporter.yaml
```

## Grafana dashboards:
https://grafana.com/grafana/dashboards/1860
https://grafana.com/grafana/dashboards/14057
https://github.com/prometheus/alertmanager/blob/main/template/default.tmpl

# Gitlab CI Pipeline Monitoring
## Update configure:
```bash
ansible-playbook -i servers reload-gitlab-pipeline-exporter.yaml
```


## References
* https://github.com/mvisonneau/gitlab-ci-pipelines-exporter
