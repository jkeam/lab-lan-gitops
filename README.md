# Lab Lan GitOps

Homelab Gitops Repo

## Apache Server

```shell
oc apply -f ./httpd-app.yaml
```

## Windows 10

```shell
oc apply -f ./windows10.yaml
```

Run `D:\virt-win-gt-x64` to install virtio drivers.
Then look for `Ethernet Settings` and update `Network 2` and set

```
IP assignment: Manual
IPv4 address: 192.168.1.204
IPv4 subnet prefix length: 24
IPv4 gateway: 192.168.1.1
IPv4 DNS servers: 192.168.1.201, 1.1.1.1
```

And lastly enable `Allow remote connections to this computer`
and then check `Firewall` and `Allow an app through a firewall`
and enable all `Remote Desktop`.

## Fedora

```shell
oc apply -f ./fedora.yaml
```

## Apps

```shell
oc apply -f ./apps-helm-repo.yaml

# example app from helm chart repo above
oc apply -f ./hello-go.yaml
```
