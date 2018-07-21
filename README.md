[![Build Status](https://travis-ci.org/while-true-do/ansible-role-repo-collabora-code.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-repo-collabora-code)

# Ansible Role: repo-collabora-code
| A role that installs the yum repository for Collabora Online - CODE from official collaboraoffice.com

## Motivation

This role is needed to provide the Collabora Online - CODE packages.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while_true_do/repo_collabora_code)

```
ansible-galaxy install while_true_do.repo_collabora_code
```

Install from [Github](https://github.com/while-true-do/ansible-role-repo-collabora-code)

```
git clone https://github.com/while-true-do/ansible-role-repo-collabora-code.git while_true_do.repo_collabora_code
```

## Requirements

Used Modules:

-   [command_module](https://docs.ansible.com/ansible/latest/modules/command_module.html)
-   [include_tasks_module](https://docs.ansible.com/ansible/latest/modules/include_tasks_module.html)
-   [rpm_key_module](https://docs.ansible.com/ansible/latest/modules/rpm_key_module.html)
-   [yum_repository_module](https://docs.ansible.com/ansible/latest/modules/yum_repository_module.html)

## Dependencies

This role has the below dependencies:

-   <https://galaxy.ansible.com/while_true_do/yum>

You can install them with:

```
ansible-galaxy install -r requirements.yml
```

## Role Variables

```yaml
# defaults/main.yml for repo_collabora_code

# repository state can be set to "present" / "absent"
wtd_repo_collabora_code_state: "present"
```

## Example Playbook

Simple Example:

```yaml
- hosts: servers
  roles:
    - { role: while_true_do.repo_collabora_code }
```

Advanced Example:

```yaml
- hosts: servers
  roles:
    - { role: while_true_do.repo_collabora_code, wtd_repo_collabora_code_state: "absent" }
```

## Testing

All tests are located in [test directory](./tests/).

Basic testing:

```
bash ./tests/test-ansible.sh
bash ./tests/test-spelling.sh
bash ./tests/test-whitespace.sh
```

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look
at the links first.

-   [Code of Conduct](./docs/CODE_OF_CONDUCT.md)
-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-repo-collabora-code/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-repo-collabora-code/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Site: [while-true-do.org](https://while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
