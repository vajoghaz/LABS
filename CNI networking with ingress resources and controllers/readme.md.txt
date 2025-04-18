CNI networking with ingress resources and controllers

CNI networking provides the best performance since it does not require IP forwarding and UDR, and ingress controllers can be managed from within Kuberbetes. Kubenet networking requires defined routes and IP forwarding, making the network slower. Azure load balancers cannot be managed by using Kubernetes tools.

Provides the highest networking performance possible
Manages ingress traffic by using Kubernetes tools

https://learn.microsoft.com/en-gb/azure/aks/operator-best-practices-network



