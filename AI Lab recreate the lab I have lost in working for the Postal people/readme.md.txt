Lab: use case for IaaS over PaaS

AI Lab: recreate the lab I have lost in working for the Postal people.

Scenario: There are CPU types required based on workload. The PaaS service that created the underlying Azure infrastructure for ML Studio to train my models created a General type of VM in the background. It did not work. Unknown errors.

My first ARM template contained networking and a memory optinised CPU for VMSS with auto scale. ML Studio using the new definition, started to work.

Another use-case is AKS. There were so many problems with simply using the PaaS option that Microsoft essentially gave access to the underlying infrastructure in Resource Groups starting MC_SomeNamingConvention

I have some AKS Labs, I can add this to it.