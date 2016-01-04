# superlumic-mysql

Ansible role to setup rbenv on OSX. This role is part of the Superlumic project that aims to simplify repeat computer setups on OSX, 10.10 and up.

## Requirements

* OSX 10.10 or 10.11

## Dependencies

* [roderik.superlumic-homebrew](https://github.com/superlumic/ansible-role-homebrew)
* [roderik.superlumic-cli](https://github.com/superlumic/ansible-role-cli)

# Usage

Define a list of versions to install, along with their optionals gems and finally specify the default ruby version you want to use globally.

      vars:
        - rbenv_versions:
          - 1.9.3-p551
          - 2.2.3
          - 2.3.0
        - rbenv_gems_for_versions:
          - { ruby_version: '1.9.3-p551', gems: 'bundler capistrano'                    }
          - { ruby_version: '2.2.3',      gems: 'bundler capistrano pry'                }
          - { ruby_version: '2.3.0',      gems: 'bundler capistrano pry chef cocoapods' }
        - default_rbenv_version: 2.2.3

Check [Superlumic](https://github.com/superlumic/superlumic) for more documentation.

# License

GPL

# Author

[Fabien Jakimowicz](mailto:fabien@jakimowicz.com)
