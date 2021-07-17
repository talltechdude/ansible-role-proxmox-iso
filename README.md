Proxmox ISO Downloader
=========

Download ISO to Proxmox ISO path

Requirements
------------

Proxmox cluster

Role Variables
--------------

See defaults/main.yml
```
# Any valid ISO file - e.g. 
iso_url: https://github.com/rancher/k3os/releases/download/v0.20.7-k3s1r0/k3os-amd64.iso

# ISO name on disk in Proxmox
iso_name: k3os-amd64.iso

# Proxmox storage path
pve_iso_path: "/var/lib/vz/template/iso"

# Is ISO path on shared storage?
pve_iso_shared_storage: false
```

Dependencies
------------

N/A

Example Playbook
----------------

```
- name: K3os ISO | Setup
  hosts: proxmox
  roles:
    - role: talltechdude.proxmox_iso
      vars:
        iso_url: "https://github.com/rancher/k3os/releases/download/{{ k3os_version }}/k3os-amd64.iso"
        iso_name: "k3os-amd64-{{ k3os_version }}"
```

License
-------

MIT

Author Information
------------------

TallTechDude
