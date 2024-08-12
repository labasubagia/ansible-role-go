Golang
=========

Ansible role to install [Go](https://go.dev/) linux

Requirements
------------
- Ansible Core >= 2.16
- Tested Linux Distribution
  - Debian 12
  - Ubuntu 24.04
  - Fedora 40

> Note: Other distributions likely to work but not been tested

Role Variables
--------------

The following variables will change the behavior of this role (default values are shown below):

```yaml
---
go_version: "1.22.5"
go_state: present
go_packages:
  - golang.org/x/tools/gopls
  - github.com/cweill/gotests/gotests
  - github.com/fatih/gomodifytags
  - github.com/josharian/impl
  - github.com/haya14busa/goplay/cmd/goplay
  - github.com/go-delve/delve/cmd/dlv
  - github.com/golangci/golangci-lint/cmd/golangci-lint
  - honnef.co/go/tools/cmd/staticcheck
```


Example Playbook
----------------
```yaml
- hosts: servers
  roles:
    - role: labasubagia.go
      vars:
        go_version: "1.22.6"
        go_packages:
          - golang.org/x/tools/gopls
```

License
-------

MIT

Author Information
------------------

[Laba Subagia](https://github.com/labasubagia)
