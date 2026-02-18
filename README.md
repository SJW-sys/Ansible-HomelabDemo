# Ansible
Config management and policy enforcement for systems.

## Deployment

### Prerequisite in a deployment of this exact repo
- Gitlab and a runner are Deployed and configured to talk to target server
- Some Variables have been configured within Gitlab to inject into a pipeline at runtime
- target server at a minimum has docker and openssh server (w/ .pub key) setup
- DNS resolver is already configured
- Updating .env file for your needs
- using [Caddy](https://github.com/SJW-sys/Caddy-HomelabDemo) or a Reverse Proxy to handle SSL for a clean URL and encryption.

### Ansible Install
We will be deploying on a debian (13.3 trixie) linux system that is up to date and has the following preinstalled: sudo installed, account with sudo level permissions.

1) install

    sudo apt install -y ansible

## Resources:
- Github: https://github.com/ansible/ansible
- DockerHub: https://hub.docker.com/r/ansible/ansible   (Not our deployment method)
- website: https://www.redhat.com/en/ansible-collaborative
- Documentation: https://docs.ansible.com/
- Recommended Learning Resource: https://youtube.com/playlist?list=PLT98CRl2KxKEUHie1m24-wkyHpEsa4Y70 (Learn Linux TV: Ansible playlist)

## FAQ for repo visitors
### Why does the repo have 'Demo' in the title?
this "demo" repo is based on real world local deployments in my Homelab. Some settings may be changed, or different for privacy and safety.

### Where can I find more about this project and your thought process?
I make it a habit that my files typically have dozens of in-line comments to better help anyone using them for the first time to understand what is happening, maybe not always why. Also please check out my blog, it typically has more information on my projects (sometimes the post is still being planned).

### Does ths connect to your other Homelab Demo repos?
Not this one.

### Was AI used to generate this?
In part, I used it for rapid iteration and deployment of several playbooks. However many were self made and designed, but I have learned and expanded my knowledge of the tools within this project (and prior projects) with AI to design a better solution and skills for other deployments. AI I see as a tool and resource that is loose in the market place regardless of your stance, that you need to follow, know how to use, while educating others on its complexities and putting safeguards around it. I firmly design and deploy with my own brainstorming, knowledge, and troubleshooting as my first approach, but i have used AI to troubleshoot, help expand understanding, research, interpreter (ie. Bash to Go), rapid scaling and experimented with vibe coding. I have deeper thoughts and opinions, but those are better discussed rather than a few sentences in a git repo. 

## Issues to note with this "demo"
I wanted to do a proper code repo that could be poke around so you could see commits and pulls that you might normally see in a team production repo, unfortunately due to the overhead and this [issue](https://github.com/orgs/community/discussions/6292), I will be "cutting corners" and doing everything locally then pushing to main directly from my machine. However, I will still leave the demo "main" and "test" branches with there protections.

## Docker features, CI/CD tooling/skills, and other tools leveraged in this project.
- Ansible
- Yaml
- Git
- Gitlab interface and secret management
- Pipelines (all in Gitlab formatting)
- Git CD/CI best practices (branches, branch protections, etc)
- Linux (general and permissions)
- Bash
- SSH
- Documentation
