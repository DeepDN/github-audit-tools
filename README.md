# GitHub Org Audit Tool
This is a tool for auditing github organizations including their repos, users, and teams. It is useful for compliance, security and auditing.

## Capabilities
* Repo list
* Team list
* Team repo rights list
* User list
* User repo rights list

[LICENSE](./LICENSE)

## Installation
Please note that you'll need your github org name and to create a github token with access to all repo, team, and user info.

```sh
$ git clone https://github.com/DeepDN/github-audit-tools.git
$ cd github-audit-tools
$ sudo apt install python3-virtualenv  # Run this command if python3-virtualenv is not installed on your system.
$ virtualenv -p python3 venv
$ source venv/bin/activate
$ sudo apt update && sudo apt install build-essential libffi-dev python3-dev 
$ pip install -r requirements.txt
$ export GITHUB_ORG_NAME=<your github org name>   # Organization name from github account
$ export  GITHUB_TOKEN=<your github token>     # Github access token of your account
$ python github-reporting-tool.py

OPTIONAL
$ python github-reporting-tool.py > output.txt  # If you want to save output in external file then run this command

```

## Example Output
```
Repo List:
   git://github.com/DeepDN/Devops.git
   git://github.com/DeepDN/onetwotest.git
   git://github.com/DeepDN/laughing-pancake.git
   git://github.com/DeepDN/potential-octo-computing-machine.git
   git://github.com/DeepDN/literate-octo-system.git
   git://github.com/DeepDN/github-audit-tool.git
   git://github.com/DeepDN/test.git
   git://github.com/DeepDN/foo.git
   git://github.com/DeepDN/bar.git
   git://github.com/DeepDN/baz.git

Team List:
    a-team
      git://github.com/DeepDN/test.git
    b-team
      git://github.com/DeepDN/onetwotest.git
      git://github.com/DeepDN/UnstoppableDevOps.git
    bar team
      git://github.com/DeepDN/laughing-pancake.git
    foo team
      git://github.com/DeepDN/literate-octo-system.git
    gorakTeam
      git://github.com/DeepDN/onetwotest.git

Team Membership List:
   a-team  Team Members:
       bfrancom
       jesse-DeepDN
   b-team  Team Members:
       bfrancom
       jesse-DeepDN
   bar team  Team Members:
       bfrancom
       jesse-DeepDN
   foo team  Team Members:
       bfrancom
       jane-at-DeepDN
   gorakTeam  Team Members:
       bfrancom
       jane-at-DeepDN
       
Direct Repo Rights:
   git://github.com/DeepDN/UnstoppableDevOps.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/onetwotest.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/laughing-pancake.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/potential-octo-computing-machine.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/literate-octo-system.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/github-audit-tool.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/test.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/foo.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/bar.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
   git://github.com/DeepDN/baz.git
       bfrancom
       jesse-DeepDN
       jane-at-DeepDN
```
