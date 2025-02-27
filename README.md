# Helm Chart Cheatsheet

## **Helm Overview**
Helm is a package manager for Kubernetes that helps deploy applications using charts.

### **Helm Components**
1. **Helm Client** – Command-line tool for managing Helm charts.
2. **Helm Chart** – A package containing Kubernetes resources.
3. **Chart Repository** – A storage for Helm charts.
4. **Release** – A deployed Helm chart in a Kubernetes cluster.

---

## **Common Helm Commands**

### **Managing Helm Repositories**
```sh
helm repo add <repo_name> <repo_url>     # Add a new Helm repository
helm repo list                            # List all repositories
helm repo update                          # Update the repository index
helm search repo <chart_name>             # Search for charts in the repository
```

### **Installing and Upgrading Charts**
```sh
helm install <release_name> <chart>      # Install a Helm chart
helm install <release_name> <chart> -f values.yaml  # Install using custom values
helm upgrade <release_name> <chart>      # Upgrade a release
helm rollback <release_name> <revision>  # Rollback to a previous release
```

### **Managing Releases**
```sh
helm list                                # List all deployed releases
helm status <release_name>               # Check the status of a release
helm history <release_name>              # View the history of a release
helm uninstall <release_name>            # Uninstall a release
```

### **Working with Helm Charts**
```sh
helm create <chart_name>                 # Create a new Helm chart
helm package <chart_name>                # Package a Helm chart into a .tgz file
helm lint <chart_name>                   # Validate the Helm chart
helm template <chart_name>               # Render templates locally
```

### **Customizing Helm Charts**
```sh
helm show values <chart>                 # Show default values of a chart
helm get values <release_name>           # Get values of a deployed release
helm upgrade <release_name> <chart> -f custom-values.yaml  # Upgrade using custom values
```

### **Debugging and Troubleshooting**
```sh
helm get manifest <release_name>         # View the manifest of a release
helm get notes <release_name>            # View post-installation notes
helm get hooks <release_name>            # View lifecycle hooks
helm get all <release_name>              # Get all details of a release
```

---

## **Useful Resources**
- [Helm Official Docs](https://helm.sh/docs/)
- [Helm Hub](https://artifacthub.io/)
- [Kubernetes Official Docs](https://kubernetes.io/docs/)

---

This cheatsheet provides a quick reference for working with Helm charts in Kubernetes. Let me know if you have any suggestions or improvements!
