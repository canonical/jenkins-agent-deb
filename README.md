The jenkins-agent package is vailable at: https://launchpad.net/~canonical-is-devops/+archive/ubuntu/jenkins-agent-charm

# Installation
Follow the instruction in the PPA archive to install the package
```
sudo add-apt-repository ppa:tphan025/ppa
sudo apt update
sudo apt install jenkins-agent
```

# Configuration
The jenkins-agent service requires 3 environment variables to be set: `JENKINS_URL`, `JENKINS_AGENT` and `JENKINS_TOKEN`