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

Copyright 2015 VMware, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

