# multipass-playground

## Installation

```
brew install --cask multipass
```

## Launch Ubuntu

```
multipass launch --name ubuntu-instance --cloud-init cloud-config.yml
multipass shell ubuntu-instance
```

## Check self ip

```
ubuntu@ubuntu-instance:~$ hostname -I | awk '{print $1}'
192.168.x.x
```

## Debugging

Look in `/var/log/cloud-init-output.log`.
It Captures the output from each stage of cloud-init when it runs.

# References

- [cloud-init documentation](https://cloudinit.readthedocs.io/en/latest/index.html)
- [GitHub - canonical/multipass: Multipass orchestrates virtual Ubuntu instances](https://github.com/canonical/multipass)
