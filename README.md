# systemd-coredump

This role configures systemd-coredump.

## Requirements

systemd with coredump compiled in

## Role Variables

| Name                         | Default/Required | Description                                 |
|------------------------------|:----------------:|---------------------------------------------|
| `coredump_storage`           | `external`       | Coredump storage to use                     |
| `coredump_compress`          | `yes`            | Whether to compress the coredumps           |
| `coredump_process_max_size`  | `2G`             | Maximum process size to keep                |
| `coredump_external_max_size` | `2G`             | Maximum process size to keep external       |
| `coredump_journal_max_size`  | `767M`           | Maximum process size to keep in the journal |
| `coredump_max_use`           |                  | Maximum amount of disk space to use         |
| `coredump_keep_free`         |                  | Keep this amount of disk space free         |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
  - systemd-coredump
    coredump_storage: none
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

## Author Information

- [Janne Heß](https://github.com/dasJ)
