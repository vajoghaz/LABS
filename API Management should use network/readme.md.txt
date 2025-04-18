I would do the APIOps lab. It seems than not only the NodeJS version is updated in the run pipeline YAMLs but the old version specified for NPM is disappeared as well. It now contains a generic install without specifying the version - which was v3

The original deployment had a VNet integration

API Management services should use a virtual network
Description: Azure Virtual Network deployment provides enhanced security, isolation, and allows you to place your API Management service in a non-internet routable network that you control access to. These networks can then be connected to your on-premises networks using various VPN technologies, which enable access to your backend services within the network and/or on-premises. The developer portal and API gateway can be configured to be accessible either from the Internet or only within the virtual network. (Related policy: API Management services should use a virtual network).

Severity: Medium

https://github.com/MicrosoftDocs/azure-security-docs/blob/main/articles/defender-for-cloud/recommendations-reference-data.md#api-management-services-should-use-a-virtual-network

The directory for a series of related labs would involve dissecting the extractor exe.

