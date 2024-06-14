# Ansible Collection - eduardolmedeiros.azcopy_collection

This collection install azcopy binary from microsoft repository.

[AzCopy](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10) is a command-line utility created and maintained by [Microsoft](https://www.microsoft.com) that you can use to copy blobs or files to or from a storage account.

## Requirements

* This role supports: CentOS 7, AlmaLinux 8/9, RockyLinux 8/9, Ubuntu, Debian, or Red Hat Enterprise Linux distribution.
* Ansible 2.9 or higher.

## Role Variables

All "standards" variables are defined on roles/azcopy/defaults/main.yml.
If you want to replace or change some variable, please change on playbook level.

```
| variable           | description              | default        |
|--------------------|--------------------------|----------------|
| azcopy_pkg_deps    | package dependencies     | unzip          |
| azcopy_username    | azcopy username          | root           |
| azcopy_group       | azcopy group name        | root           |
| azcopy_bin_path    | installation path        | /usr/local/bin |
| azcopy_pkg_url     | azcopy source url        |                |
```

## Dependencies

N/A

## Install collection

```
ansible-galaxy collection install eduardolmedeiros.azcopy_collection
```

## Example Playbook

```
- hosts: all
  collections: 
    - eduardolmedeiros.azcopy_collection
  tasks:
    - name: "Include azcopy role"
      include_role:
        name: "azcopy"
```

## License

MIT

## Author Information

[Eduardo Medeiros](https://www.emedeiros.me/)
