# common

Common server configuration

## Requirements

Works on ubuntu.

## Role Variables

* `common_base_pkgs` - An array of base pkgs
* `common_dev_ops_keys` - An array of authorized keys for ssh
* `common_dev_ops_keys_exclusive` - Flag whether to clobber any existing keys (False by default)
* `common_motd_title` - A message displayed at login

## Example usage

In a playbook:

    - hosts: appservers
      roles:
        - role: thermistor.common
          common_base_pkgs:
            - fortune
          common_dev_ops_keys:
            - "{{ lookup('file', 'files/ssh_keys/yourkey.pub') }}"
          common_motd_title: 'Hello'

## License

Licensed under the MIT License. See the LICENSE file for details.
