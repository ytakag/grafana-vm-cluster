# grafana-vm-cluster

## Install

```bash
cd ansible
ansible-galaxy collection install -r requirements.yml
```

## Usage

```bash
cd ansible
ansible-playbook playbook.yml
```

## Ref

### Multitenancy

- select
  - http://`<vmauth-read>`:8427/select/multitenant/prometheus
  - http://`<vmauth-read>`:8427/select/`<vm_account_id>`:`<vm_project_id>`/prometheus
- insert
  - http://`<vmauth-write>`:8427/insert/multitenant/prometheus/api/v1/write
  - http://`<vmauth-write>`:8427/insert/`<vm_account_id>`:`<vm_project_id>`/prometheus/api/v1/write

|vm_account_id|用途|
|--|--|
|0|監視基盤|

|vm_project_id|用途|
|--|--|
|0|監視基盤|
