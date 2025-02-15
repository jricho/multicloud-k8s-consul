

## get creds for AKS and merge kubeconfig
az aks get-credentials --resource-group $(terraform output -raw resource_group_name) --name $(terraform output -raw kubernetes_cluster_name)

## stop AKS
az aks stop --name regular-rodent-k8s --resource-group regular-rodent-k8s
