![Logo](https://raw.githubusercontent.com/idealista/azkaban-role/master/logo.gif)

[![Build Status](https://travis-ci.org/idealista/azkaban-role.png)](https://travis-ci.org/idealista/azkaban-role)

# Azkaban Ansible role

This ansible role installs an Azkaban web server / executor server in a debian environment.

This role uses [Azkaban Ldap UserManager](https://github.com/researchgate/azkaban-ldap-usermanager) to enable LDAP user manager support.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your ansible playbook. Once launched, it will install an [Azkaban](https://azkaban.github.io) web server / executor server in a Debian system.

### Prerequisities

Ansible 2.4.5.0 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Docker](https://www.docker.com/) are used. Check `test-requirements.txt` for Ansible, Molecule and Docker Python module versions.

### Installing

Create or add to your roles dependency file (e.g requirements.yml) from GitHub:

```
- src: http://github.com/idealista/azkaban-role.git
  scm: git
  version: 1.0.0
  name: azkaban
```

or using [Ansible Galaxy](https://galaxy.ansible.com/idealista/azkaban-role/) as origin if you prefer:

```
- src: idealista.azkaban-role
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
---
- hosts: someserver
  roles:
    - { role: azkaban }
```

## Usage

Look to the defaults properties file to see the possible configuration properties.

## Testing

```
pipenv install -r test-requirements.txt --python 2.7
pipenv run molecule test --all
```

See molecule.yml to check possible testing platforms.

## Built With

![Ansible](https://img.shields.io/badge/ansible-2.4.5.0-green.svg)
![Molecule](https://img.shields.io/badge/molecule-2.20.0-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/azkaban-role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/azkaban-role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
