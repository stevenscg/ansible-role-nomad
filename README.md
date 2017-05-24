# Ansible role to install HashiCorp Nomad

This Ansible role installs/updates and configures nomad


## Variables


```yml
# This is not used when using a root token (on dev, etc)
nomad_vault_create_from_role: nomad-cluster
```

## Usage

```yml
- role: nomad
  nomad_server: true
  nomad_client: true
  nomad_region: local
  nomad_datacenter: local
  nomad_server_bootstrap_expect: 1
  nomad_leave_on_interrupt: true
  nomad_client_auto_join: true
  nomad_server_auto_join: true
  nomad_vault_enabled: true
  nomad_consul_auto_advertise: true
  nomad_client_options:
    docker.auth.config: /home/nomad/.docker/config.json
    driver.raw_exec.enable: "1"
    driver.exec: "1"
  tags:
    - nomad
```


## License

MIT
