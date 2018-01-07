# `dotfiles-role-i3`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-role-i3.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-role-i3)
[![GitHub tag](https://img.shields.io/github/tag/thecjharries/dotfiles-role-i3.svg)](https://github.com/thecjharries/dotfiles-role-i3)

## Requirements

Fedora 27 is recommended.

## Role Variables

Defaults are below.

```yml
---
owning_user: "{{ ansible_user }}"
owning_group: "{{ ansible_user }}"
root_dir: "/home/{{ ansible_user }}"
config_dir: "{{ root_dir }}/.config"
```

Additionally, these `vars` are set:

```yml
---
needed_packages:
  - i3
  - i3status
  - dmenu
  - i3lock
  - feh
  - conky
```

## Dependencies

```yml
---
- src: git+https://github.com/thecjharries/dotfiles-role-common-software.git
- src: git+https://github.com/thecjharries/dotfiles-role-package-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-generic-template.git
- src: git+https://github.com/thecjharries/dotfiles-role-git.git
- src: git+https://github.com/thecjharries/dotfiles-role-sublime.git
- src: git+https://github.com/thecjharries/dotfiles-role-terminator.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: dotfiles-role-i3
```

## License

ISC
