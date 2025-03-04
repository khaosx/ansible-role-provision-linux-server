# Ansible Role: provision_linux_server

An Ansible role that applies full provisioning to a newly built Ubuntu server.

## Requirements

- Ansible 2.9 or higher
- Supported Platforms:
  - Ubuntu 22.04 LTS (Jammy)
  - Ubuntu 24.04 LTS (Noble)
- The target machine should have internet access to download packages and repositories.

## Role Variables

| Variable                           | Default Value           | Description                                                  |
| ---------------------------------- | ----------------------- | ------------------------------------------------------------ |
| `blacklist_wireless_pi`            | `false`                 | Whether to blacklist wireless on Raspberry Pi.               |
| `apt_install_packages`             | List of packages        | List of packages to install via apt.                         |
| `ntp_timezone`                     | `America/New_York`      | Timezone for NTP configuration.                              |
| `ntp_primary`                      | `palladium.khaosx.io`   | Primary NTP server.                                          |
| `ntp_secondary`                    | `time.apple.com`        | Secondary NTP server.                                        |

## Installation

`ansible-galaxy role install khaosx.provision-linux-server`

## Example Playbook

```yaml
---
- name: Provision server to prepare for app deployment
  hosts: linux_servers
  become: yes
  roles:
    - role: provision_linux_server
```

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Author Information
Created by [Kristopher Newman](https://github.com/khaosx)  
GitHub Repository: [ansible-role-provision-linux-server](https://github.com/khaosx/ansible-role-provision-linux-server)  
Ansible Galaxy: [khaosx.provision-linux-server](https://galaxy.ansible.com/ui/standalone/roles/khaosx/plex-server/documentation/)

## Contributing
Contributions are welcome! If you have improvements or feature requests, please open an issue or submit a pull request on GitHub.

1. Fork the repository on GitHub.
2. Create a new branch for your feature or bugfix.
3. Write your code and tests.
4. Submit a pull request with a clear description of your changes.

## Issues
For any issues, questions, or suggestions, please open an issue on GitHub.
