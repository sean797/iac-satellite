# iac-satellite
Infra as Code deployment of Satellite using Ansible


## Requirements

- All Satellite nodes should meet the minimum requirements as set out in https://access.redhat.com/documentation/en-us/red_hat_satellite/6.1/html-single/installation_guide/index#sect-Red_Hat_Satellite-Installation_Guide-Prerequisites
take special care of the *Storge* section

## Initial instructions

1. `ansible-galaxy install -r requirements.yml`

1. `ansible-playbook playbooks/satellite-build.yml`

NOTE: First run should also include `-e configure_katello_force_manifest_upload=True` to fix this we need to use a different manifest for each Satellite, for the POC we are just using the same one across all nodes.
