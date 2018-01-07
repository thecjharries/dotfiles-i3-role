# `dotfiles-i3-role`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-i3-role.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-i3-role)

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
- src: git+https://github.com/thecjharries/dotfiles-common-software-role.git
- src: git+https://github.com/thecjharries/dotfiles-package-installer-role.git
- src: git+https://github.com/thecjharries/dotfiles-generic-template-role.git
- src: git+https://github.com/thecjharries/dotfiles-git-role.git
- src: git+https://github.com/thecjharries/dotfiles-sublime-role.git
- src: git+https://github.com/thecjharries/dotfiles-terminator-role.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: dotfiles-i3-role
```

## License

ISC
