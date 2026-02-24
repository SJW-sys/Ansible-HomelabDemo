# Ansible
Self-host Ansible for config management and policy enforcement

## Deployment

### Ansible Install
We will be deploying on a debian (13.3 trixie) linux system that is up to date and has the following preinstalled: sudo installed, account with sudo level permissions.

1) install

    sudo apt install -y ansible

### Setup

1) get files on your server

    sudo git clone https://dev.home.bbhomeworld.com/homelab/ansible.git

2) Review anything you plan to execute

3) run your ansible playbook against local host (Change PLAYBOOK to any of the files I have provided)

    sudo ansible-playbook ~./DeploymentFiles/Ansible/Playbooks/PLAYBOOK.yml -i localhost, --connection=local

If you have ssh connections and your inventory file (example provided) configured you can target remote host with ansible playbooks. If you setup cron with ansible commands, you can have playbooks execute against host to keep them inline with policy standards. You can also use a ansible.cfg file (example provided) at the root of your playbook directory to provided service wide variables.

### Notes on my personal deployment
Ansible is deployed via a gitlab runner on a host system, that has several task setup to run regularly via cron to keep my homelab policies and configuration in-line with current standards. I use about a dozen dedicated playbooks to more focused ask, I don't want scope creep on my playbooks. I do rely on ansible.cfg and inventory files as well to help keep everything in working order.

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
Not this project.

### Was AI used to generate this?
In part, I used it for going back and forth on tweaking example Inventory and ansible.cfg files that I use and have provided bases for here. Otherwise all the other files were made and designed, but I have learned and expanded my knowledge of the tools within this project (and prior projects) with AI to design a better solution and skills for other deployments. AI I see as a tool and resource that is loose in the market place regardless of your stance, that you need to follow, know how to use, while educating others on its complexities and putting safeguards around it. I firmly design and deploy with my own brainstorming, knowledge, and troubleshooting as my first approach, but i have used AI to troubleshoot, help expand understanding, research, interpreter (ie. Bash to Go), rapid scaling and experimented with vibe coding. I have deeper thoughts and opinions, but those are better discussed rather than a few sentences in a git repo. 

## Docker features, CI/CD tooling/skills, and other tools leveraged in this project.
- ansible
- Yaml
- Git
- Gitlab interface and secret management
- Pipelines (all in Gitlab formatting)
- Git CD/CI best practices (branches, branch protections, etc)
- Linux (general and permissions)
- Bash
- SSH
- Documentation
