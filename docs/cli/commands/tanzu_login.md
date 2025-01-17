## tanzu login

Login to the platform

```
tanzu login [flags]
```

### Examples

```

	# Login to TKG management cluster using endpoint
	tanzu login --endpoint "https://login.example.com"  --name mgmt-cluster

	# Login to TKG management cluster by using kubeconfig path and context for the management cluster
	tanzu login --kubeconfig path/to/kubeconfig --context path/to/context --name mgmt-cluster

	# Login to TKG management cluster by using default kubeconfig path and context for the management cluster
	tanzu login  --context path/to/context --name mgmt-cluster

	# Login to an existing server
	tanzu login --server mgmt-cluster

	[*] : User has two options to login to TKG. User can choose the login endpoint option
	by providing 'endpoint', or user can choose to use the kubeconfig for the management cluster by
	providing 'kubeconfig' and 'context'. If only '--context' is set and '--kubeconfig' is unset
	$KUBECONFIG env variable would be used and, if $KUBECONFIG env is also unset default 
	kubeconfig($HOME/.kube/config) would be used
	
```

### Options

```
      --apiToken string     API token for global login
      --context string      the context in the kubeconfig to use for management cluster. Valid only if user doesn't choose 'endpoint' option.(See [*]) 
      --endpoint string     endpoint to login to
  -h, --help                help for login
      --kubeconfig string   path to kubeconfig management cluster. Valid only if user doesn't choose 'endpoint' option.(See [*])
      --name string         name of the server
      --server string       login to the given server
```

### SEE ALSO

* [tanzu](tanzu.md)	 - 
* [tanzu login completion](tanzu_login_completion.md)	 - Generate the autocompletion script for the specified shell

###### Auto generated by spf13/cobra on 14-Sep-2022
