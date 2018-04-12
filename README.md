# ansible-role-logstash

Tested on Ansible 2.4.2 and Ubuntu 16.04

This role depends on a
[docker](https://github.com/blurblah/ansible-role-docker) role and installs logstash running on a docker container.

Referenced by a
[Configuring Logstash for Docker](https://www.elastic.co/guide/en/logstash/6.2/docker-config.html) document.

## Playbook sample
This sample playbook installs logstash.

* **http_port (optional)** : default is 9600
* **logstash_input_port (optional)** : default is 5044
* **client_inactivity_timeout (optional)** : default is 60 (secs)
* **es.host (optional)** : default is the host ip to be installed logstash
* **es.port (optional)** : default is 9200
* **version (optional)** : default is 6.2.3

```yaml
- hosts: logstash_host
  become: yes
  roles:
    - role: logstash
```
