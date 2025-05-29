# kubectl Commands Cheat Sheet

## Cluster Info

- **Show cluster info**
  ```
  kubectl cluster-info
  ```

- **View nodes**
  ```
  kubectl get nodes
  ```

## Context & Configuration

- **List contexts**
  ```
  kubectl config get-contexts
  ```

- **Switch context**
  ```
  kubectl config use-context <context-name>
  ```

## Namespace

- **List namespaces**
  ```
  kubectl get namespaces
  ```

- **Set default namespace**
  ```
  kubectl config set-context --current --namespace=<namespace>
  ```

## Pods

- **List pods in current namespace**
  ```
  kubectl get pods
  ```

- **List pods in all namespaces**
  ```
  kubectl get pods --all-namespaces
  ```

- **Describe pod**
  ```
  kubectl describe pod <pod-name>
  ```

- **Get pod logs**
  ```
  kubectl logs <pod-name>
  ```

- **Get logs from a specific container in a pod**
  ```
  kubectl logs <pod-name> -c <container-name>
  ```

- **Get logs from previous (crashed) container**
  ```
  kubectl logs <pod-name> --previous
  ```

- **Stream logs (follow)**
  ```
  kubectl logs -f <pod-name>
  ```

- **Get logs for all pods with a label**
  ```
  kubectl logs -l <label-selector>
  ```

- **Get logs from a specific namespace**
  ```
  kubectl logs <pod-name> -n <namespace>
  ```

- **Execute command in pod**
  ```
  kubectl exec -it <pod-name> -- bash
  ```

- **Delete pod**
  ```
  kubectl delete pod <pod-name>
  ```

## Deployments

- **List deployments**
  ```
  kubectl get deployments
  ```

- **Describe deployment**
  ```
  kubectl describe deployment <deployment-name>
  ```

- **Scale deployment**
  ```
  kubectl scale deployment <deployment-name> --replicas=<number>
  ```

- **Update deployment (rolling restart)**
  ```
  kubectl rollout restart deployment <deployment-name>
  ```

- **Delete deployment**
  ```
  kubectl delete deployment <deployment-name>
  ```

## Services

- **List services**
  ```
  kubectl get services
  ```

- **Describe service**
  ```
  kubectl describe service <service-name>
  ```

- **Expose deployment as service**
  ```
  kubectl expose deployment <deployment-name> --type=<type> --port=<port>
  ```

## ConfigMaps & Secrets

- **List ConfigMaps**
  ```
  kubectl get configmaps
  ```

- **Describe ConfigMap**
  ```
  kubectl describe configmap <configmap-name>
  ```

- **List Secrets**
  ```
  kubectl get secrets
  ```

- **Describe Secret**
  ```
  kubectl describe secret <secret-name>
  ```

## Apply, Edit, and Delete

- **Apply changes from YAML**
  ```
  kubectl apply -f <file.yaml>
  ```

- **Edit resource**
  ```
  kubectl edit <resource>/<name>
  ```

- **Delete resource**
  ```
  kubectl delete -f <file.yaml>
  ```

## Miscellaneous

- **Get all resources in namespace**
  ```
  kubectl get all
  ```

- **Get resource YAML**
  ```
  kubectl get <resource> <name> -o yaml
  ```

- **Port-forward pod**
  ```
  kubectl port-forward <pod-name> <local-port>:<pod-port>
  ```

---

**Tip:**  
Replace `<pod-name>`, `<deployment-name>`, `<service-name>`, `<file.yaml>`, `<namespace>`, etc., with your actual resource names.
