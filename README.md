# ansible-role-vrpt

Ansible playbook to automate installing, running and maintaining vRPT as
container(s).

## Requirements

This role currently requires a working Docker Engine and access to the
registry for pulling the images.

## Role Variables

```yaml
# Container memory limit. Use 512MB, type string, or 0 for unlimited
vrpt_memory_limit: 0MB

# The container image to create and use.
vrpt_docker_image: openedge/vrpt

# The docker CMD to use for running the container.
# The default setting is a script injected during the build of the image.
vrpt_docker_command: "/start.sh"
```

## Example playbook

```
---
- hosts: vrpt
  sudo: True
  roles:
    - vrpt
  vars:
    - ... forthcoming
```

# License and Copyright

Copyright 2015 VMware, Inc.  All rights reserved.

SPDX-License-Identifier: Apache-2.0 OR GPL-3.0-only

This code is Dual Licensed Apache-2.0 or GPLv3

