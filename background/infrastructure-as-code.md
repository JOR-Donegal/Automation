# Infrastructure as Code

With a knowledge of scripting, comes the capability to configure devices and services consistently and repeatedly, on demand, either with a single instruction or as part of an automated process. This approach can be taken with almost any equipment which has a CPU and memory and is configurable.&#x20;

For example, in the electricity industry, the instrumentation of a plant may be defined using IEC61850; the entire sub-station and electrical plant is abstracted into an XML structure. The physical design is done by an electrical engineer, using a GUI. A network engineer needing to provision the communications and security for such a plant can extract the information needed for configuration directly from the XML structure, communications and security equipment can be configured automatically \[1].&#x20;

If an infrastructure is based on virtual machines, it is possible to configure the entire infrastructure based on machine readable configuration files. With a single script, it is possible to provision servers and services and then configure and deploy them. It is equally possible to create and configure the underlying communications and security infrastructure. This is infrastructure as code.&#x20;

As the cloud revolution occurred, it became more important to be able to create infrastructures on demand. As software models changed and the move to the DevOps culture began, it became critical that just as software deployment could be automated, so too should infrastructure.

Interrogation of equipment may be as important as configuration. Documentation is prone to error and omission. In many cases, the equipment in use is the best definition of the capabilities and state of the equipment. Any new approach to configuration should include the ability to extract the data schema directly from the device and to populate that schema with values.&#x20;

For any substantial project in Amazon AWS, Microsoft Azure, or in private cloud, we no longer configure by hand. We automate configuration and the further back we can abstract, the better!



\[1] J. O’Raw, D. M. Laverty, D. J. Morrow, “IEC 61850 Substation Configuration Language as a basis for Automated Security and SDN Configuration”, presented at PESGM, Chicago, July 2017
