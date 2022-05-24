# Role Name

_A brief description of the role goes here._

## Requirements

_Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required._

## Role Variables

```yml
kubernetes_setup_server: true
kubernetes_setup_agent: false
kubernetes_fetch_k3s_yaml: false

kubernetes_token:
kubernetes_port: 6443
kubernetes_server_dns_name:
kubernetes_server_ip:
kubernetes_server_args: --no-deploy traefik

kubernetes_agent_ip:
kubernetes_agent_args: --kubelet-arg node-status-update-frequencey=5s

kubernetes_install_url: https://get.k3s.io

kubernetes_config_server_path: /etc/rancher/k3s/k3s.yaml
kubernetes_config_local_path: ~/.kube
```

## Dependencies

_A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles._

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: kubernetes
  roles:
    - role: kubernetes
      kubernetes_setup_server: true
      kubernetes_setup_agent: false
      kubernetes_fetch_k3s_yaml: false
      kubernetes_token: ...
      kubernetes_server_dns_name: ...
      kubernetes_server_ip: ...
      kubernetes_agent_ip: ...
```

## License

GNU AFFERO GENERAL PUBLIC LICENSE

## Author Information

MVladislav
