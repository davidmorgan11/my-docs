# Linux

## Borg Backup

### Backup Script
```bash
#!/bin/sh
REPOSITORY=borg@borg:{hostname}

BORG_PASSPHRASE='%C2EYS$k-u=:r' borg create --progress -v --list --compression zlib,6 $REPOSITORY::'{hostname}-{now:%Y-%m-%d}' /etc /usr/local/bin /home/user --exclude /home/user/Downloads 

BORG_PASSPHRASE='%C2EYu=:r' borg prune -v $REPOSITORY --prefix '{hostname}-' \
        --keep-daily=7 --keep-weekly=4 --keep-monthly=6
```
### Crontab
```bash
# m h  dom mon dow   command
01  8   *   *   *    rsync -avzP --delete /home/borg/mybackup borg@mydomain.com:/home/borg/
```