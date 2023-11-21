# Azure AKS with Nginx ingress and External DNS

## Architecture Diagram

![Azure AKS with Nginx ingress and External DNS](arch-diagram/Azure%20AKS%20Nginx%20ingress%20and%20External%20DNS.png)

---

The Azure AKS Nginx ingress and External DNS architecture is a robust and scalable way to expose your AKS applications to the public internet. It is a combination of the following components:

- **Azure Kubernetes Service (AKS):** A managed Kubernetes service that allows you to deploy and run containerized applications in the cloud.
- **Nginx ingress controller:** A Kubernetes Ingress controller that provides external access to your AKS applications using a single IP address.
- **External DNS:** A DNS management tool that automatically updates your DNS records to reflect the changes to your AKS cluster.

The architecture works as follows

1. The Nginx ingress controller is deployed in your AKS cluster.
2. You create Ingress resources to define the rules for routing traffic to your AKS applications.
3. External DNS watches for changes to your Ingress resources and creates or updates the corresponding DNS records in Azure DNS.
4. When a user visits the DNS name of your AKS application, they are routed to the Nginx ingress controller, which forwards the traffic to the appropriate application.

The following are some of the benefits of using the Azure AKS Nginx ingress and External DNS architecture

- **Simplified ingress configuration:** The Nginx ingress controller provides a simple and declarative way to configure ingress rules for your AKS applications.
- **Automatic DNS updates:** External DNS automatically updates your DNS records to reflect the changes to your AKS cluster, so you don't have to worry about managing DNS records manually.
- **High availability and scalability:** The Nginx ingress controller and External DNS are both highly available and scalable, so they can handle even the most demanding workloads.

The diagram also shows how External DNS uses managed identities to access Azure DNS. Managed identities are a feature of Azure Active Directory (Azure AD) that allows Azure services to access other Azure resources without requiring any credentials. This makes it easy to configure External DNS without having to manage any secrets.

Overall, the Azure AKS Nginx ingress and External DNS architecture is a powerful and flexible way to expose your AKS applications to the public internet. It provides a simple and declarative way to configure ingress rules, automatic DNS updates, and high availability and scalability.
