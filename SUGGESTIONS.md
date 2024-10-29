# Suggestions

First of all GOOD JOB!!!
It is not easy and I appreciate you  submitting this project. Below are suggestion and considerations for this and future project. Please do not take the bulletpoints too hard. These are suggestions, which are suppose to make your learning process to improve.

### Project
- Missing .gitignore
- Project DOES NOT do what is suppose to do: It is NOT OFF-LINE installer

### README
- Missing link to task.md
- Structure of the document is not clear.

### Shell script: `run_playbook.sh`

- Missing script description
- Missing `set -o errexit` and `set -o pipefail` configuration  for strict configuration
- Missing ip address configuration for setting destination for `hosts.txt`
- Missing user validation
  

### Playbook/Roles : `hosts.txt`

- DNS names are for existing infra >> does not work with out edit
- If suggested to be edited, then `hosts.txt` needs to be empty, otherwise user will be confused

### Playbook/Roles : `roles`

- Missing `copy` role described in README.md
- The roles are working on-line -  the script used in project is downloaded and run with params, but in network where you do not have internet access, this will not work
