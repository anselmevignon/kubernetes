## kubectl alpha diff

Diff different versions of configurations

### Synopsis


Diff configurations specified by filename or stdin between their local, last-applied, live and/or "merged" versions. 

LOCAL and LIVE versions are diffed by default. Other availble keywords are MERGED and LAST. 

Output is always YAML. 

KUBERNETES EXTERNAL DIFF environment variable can be used to select your own diff command. By default, the "diff" command available in your path will be run with "-u" (unicode) and "-N" (treat new files as empty) options.

```
kubectl alpha diff -f FILENAME
```

### Examples

```
  # Diff resources included in pod.json. By default, it will diff LOCAL and LIVE versions
  kubectl alpha diff -f pod.json
  
  # When one version is specified, diff that version against LIVE
  cat service.yaml | kubectl alpha diff -f - MERGED
  
  # Or specify both versions
  kubectl alpha diff -f pod.json -f service.yaml LAST LOCAL
```

### Options

```
  -f, --filename stringSlice   Filename, directory, or URL to files contains the configuration to diff
  -R, --recursive              Process the directory used in -f, --filename recursively. Useful when you want to manage related manifests organized within the same directory.
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --as string                        Username to impersonate for the operation
      --as-group stringArray             Group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --cache-dir string                 Default HTTP cache directory (default "/home/username/.kube/http-cache")
      --certificate-authority string     Path to a cert file for the certificate authority
      --client-certificate string        Path to a client certificate file for TLS
      --client-key string                Path to a client key file for TLS
      --cluster string                   The name of the kubeconfig cluster to use
      --context string                   The name of the kubeconfig context to use
      --insecure-skip-tls-verify         If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --kubeconfig string                Path to the kubeconfig file to use for CLI requests.
      --log-backtrace-at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log-dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files
      --match-server-version             Require server version to match client version
  -n, --namespace string                 If present, the namespace scope for this CLI request
      --password string                  Password for basic authentication to the API server
      --request-timeout string           The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
  -s, --server string                    The address and port of the Kubernetes API server
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
      --token string                     Bearer token for authentication to the API server
      --user string                      The name of the kubeconfig user to use
      --username string                  Username for basic authentication to the API server
  -v, --v Level                          log level for V logs
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO
* [kubectl alpha](kubectl_alpha.md)	 - Commands for features in alpha

###### Auto generated by spf13/cobra on 22-Nov-2017