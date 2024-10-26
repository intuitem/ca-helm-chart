## Installation 

### Add the repository

```shell
helm repo add intuitem https://intuitem.github.io/ca-helm-chart/
```

### Pulling default values

```shell
helm show values intuitem/ciso-assistant > my-values.yaml
```

### Creating a dedicated namespace

```shell
kubectl create ns ciso-assistant
```

### Install

```shell
helm install polpo intuitem/ciso-assistant -f my-values.yaml -n ciso-assistant
```

### Uninstall

```shell
helm uninstall polpo -n ciso-assistant
```


## Upgrading

When upgrading, make sure to:
1. Backup your persistent volumes
2. Update any custom values
3. Run: helm upgrade my-release . --set global.appVersion=vx.y.z
