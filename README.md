# Archived scripts from rpi-k3s

Utility scripts moved out of the `rpi-k3s` repository during cleanup. They are
kept here for reference and reuse, organized by topic.

## Layout

- `k8s/` - Kubernetes helpers (PVC migration, backups, image cleanup, Helm secrets)
- `gitea/` - Gitea mirror and org management helpers
- `network/` - EdgeRouter / VPN configuration scripts (SOPS-encrypted)
- `system/` - Node-level helpers (SSH, zram, motd, raspi config, temperature)
- `misc/` - Anything else

## Origin

Moved from `szpaczyna/rpi-k3s` in the `cleanup/dead-artifacts` PR. None of
these scripts are referenced by the main repository anymore. They may still be
useful on the cluster nodes or in personal automation.

## Notes

- Network scripts are SOPS-encrypted; decrypt with `sops -d` before use.
- `gitea/mirror_repos.py` needs the packages in `gitea/requirements.txt`.
