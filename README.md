# Ansible Role: <ROLENAME>

An Ansible role that installs and configures [role](https://link.com/), `Description of what this app does`

## Requirements

- Ansible 2.9 or higher
- Supported Platforms:
  - Debian 10 (Buster)
  - Debian 11 (Bullseye)
  - Ubuntu 20.04 LTS (Focal)
  - Ubuntu 22.04 LTS (Jammy)
- The target machine should have internet access to download packages and repositories.

## Role Variables

| Variable                           | Default Value           | Description                                                  |
| ---------------------------------- | ----------------------- | ------------------------------------------------------------ |
| `homebridge_user`                  | `homebridge`            | The system user under which Homebridge runs.                 |
| `homebridge_group`                 | `homebridge`            | The system group under which Homebridge runs.                |
| `homebridge_version`               | `latest`                | The version of Homebridge to install.                        |
| `nodejs_version`                   | `14.x`                  | The version of Node.js to install.                           |
| `homebridge_config_dir`            | `/var/lib/homebridge`   | The directory where Homebridge configuration will be stored. |

## Example Playbook

```yaml
---
- name: Install and configure Homebridge
  hosts: homebridge_servers
  become: yes
  roles:
    - role: homebridge
```

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Author Information
Created by [Kristopher Newman](https://github.com/khaosx)  
GitHub Repository: [ansible-role-plex-server](https://github.com/khaosx/ansible-role-plex-server)  
Ansible Galaxy: [khaosx.plex-server](https://galaxy.ansible.com/ui/standalone/roles/khaosx/plex-server/documentation/)

## Contributing
Contributions are welcome! If you have improvements or feature requests, please open an issue or submit a pull request on GitHub.

1. Fork the repository on GitHub.
2. Create a new branch for your feature or bugfix.
3. Write your code and tests.
4. Submit a pull request with a clear description of your changes.

## Issues
For any issues, questions, or suggestions, please open an issue on GitHub.
