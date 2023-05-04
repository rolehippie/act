# act

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/act)
[![General Workflow](https://github.com/rolehippie/act/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/act/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/act/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/act/actions/workflows/readme.yml)
[![Galaxy Workflow](https://github.com/rolehippie/act/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/act/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/act)](https://github.com/rolehippie/act/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.act-blue)](https://galaxy.ansible.com/rolehippie/act)

Ansible role to install act for local action execution.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [act_arch](#act_arch)
  - [act_download](#act_download)
  - [act_path](#act_path)
  - [act_version](#act_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### act_arch

Architecture for act binary

#### Default value

```YAML
act_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'x86_64' }}"
```

### act_download

URL to download act binary from

#### Default value

```YAML
act_download: https://github.com/nektos/act/releases/download/v{{ act_version }}/act_Linux_{{
  act_arch }}.tar.gz
```

### act_path

Path to install the binaries

#### Default value

```YAML
act_path: /usr/bin
```

### act_version

Version of act binary to install

#### Default value

```YAML
act_version: 0.2.45
```

## Discovered Tags

**_act_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
