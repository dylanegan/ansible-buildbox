# ansible-buildbox

This is an ansible role which downloads and installs [buildbox](http://buildbox.io) agent,
then configures it as a service. Currently it supports [ubuntu](http://ubuntu.com).

# Role Variables

These are the configurable attributes of the role, note you MUST configure the `buildbox_token`
otherwise the agent will fail to start.

```yaml
buildbox_arch: "amd64"
buildbox_group: "buildbox"
buildbox_home: "/home/buildbox"
buildbox_token: ""
buildbox_user: "buildbox"
buildbox_version: "1.0-beta.5"
```

# Example Playbook

```yaml
- hosts: servers
  roles:
     - { role: wolfeidau.buildbox, buildbox_token: "whatever" }
```

# License

Copyright (c) 2014 Mark Wolfe
Licensed under the MIT license.
