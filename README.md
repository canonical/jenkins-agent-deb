This repository contains the debian packaging of the `jenkins-agent` entrypoint script. It is currently meant to be used by the (jenkins-agent machine charm)[https://github.com/canonical/jenkins-agent-operator] but it can be used as a standalone package to help bootstrapping a jenkins agent on bare-metal. The package ships both a systemd service and the entrypoint executable located at `/usr/bin/jenkins-agent`

## Configure systemd service 
The systemd service can be configured via a configuration file.
```
# File: /etc/systemd/system/jenkins-agent.service.d/override.conf
[Service]
Environment="JENKINS_SECRET=secret"
Environment="JENKINS_URL=url"
Environment="JENKINS_AGENT=node-name"
```

## Configure executable
`JENKINS_URL=url JENKINS_SECRET=secret JENKINS_AGENT=node-name /usr/bin/jenkins-agent`
