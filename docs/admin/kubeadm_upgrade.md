
Upgrade your cluster smoothly to a newer version with this command.

### Synopsis


Upgrade your cluster smoothly to a newer version with this command.

```
kubeadm upgrade
```

### Options

```
      --allow-experimental-upgrades        Show unstable versions of Kubernetes as an upgrade alternative and allow upgrading to an alpha/beta/release candidate versions of Kubernetes.
      --allow-release-candidate-upgrades   Show release candidate versions of Kubernetes as an upgrade alternative and allow upgrading to a release candidate versions of Kubernetes.
      --config string                      Path to kubeadm config file. WARNING: Usage of a configuration file is experimental!
      --ignore-checks-errors stringSlice   A list of checks whose errors will be shown as warnings. Example: 'IsPrivilegedUser,Swap'. Value 'all' ignores errors from all checks.
      --kubeconfig string                  The KubeConfig file to use when talking to the cluster. (default "/etc/kubernetes/admin.conf")
      --print-config                       Specifies whether the configuration file that will be used in the upgrade should be printed or not.
```
