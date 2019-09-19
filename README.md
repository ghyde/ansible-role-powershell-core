# PowerShell Core

Install [PowerShell Core][pwsh] on Fedora ([Reference][install_fedora]).

## Role Variables

### defaults/main.yml

| name                         | description                              | type | default            |
| ---------------------------- | ---------------------------------------- | ---- | ------------------ |
| powershell_core_dependencies | List of dependencies for PowerShell Core | List | [compat-openssl10] |

### vars/main.yml

| name               | description                | type | default                                                |
| ------------------ | -------------------------- | ---- | ------------------------------------------------------ |
| microsoft_key_url  | URL for Microsoft key      | URL  | https://packages.microsoft.com/keys/microsoft.asc      |
| microsoft_repo_url | URL for Microsoft yum repo | URL  | https://packages.microsoft.com/config/rhel/7/prod.repo |

## Example Playbook

```yaml
- hosts: workstations
  tasks:
  - import_role:
      name: powershell-core
```

## License

[MIT](LICENSE)

[pwsh]: https://github.com/PowerShell/PowerShell
[install_fedora]: https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-6#fedora
