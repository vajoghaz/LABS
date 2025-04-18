Create a Private Link Service using CLI


A private link service will allow access from outside the virtual network to an endpoint by using NAT. Since you do not control the IP addressing for other virtual networks, this ensures connectivity even if IP addresses overlap. Once a private link service is used in the load balancer, other users can create a private endpoint on virtual networks to access the load balancer.


https://learn.microsoft.com/en-gb/azure/private-link/create-private-link-service-cli

Create a private link service on the virtual network and instruct users to access the cluster by using a private link endpoint in their virtual networks.

