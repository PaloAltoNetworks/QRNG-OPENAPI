# QRNG-OPENAPI
GitHub Repository for QRNG Open API


**Readme**
The QRNG Open API was created by Palo Alto Networks and six technical partners (Anametric, ID Quantique, Qrypt, Quantinuum, Quantropi, and Quside) to simplify the ability to obtain high quality entropy from an external QRNG platform (source).  The QRNG Open API provides a common mechanism to obtain information on the QRNG platform’s capabilities, retrieve entropy from the platform, and to check the health of the entropy provided.  

Much like the OASIS’s PKCS#11 standard is designed to ensure interoperability, abstraction, and flexibility when interacting with HSMs, the QRNG Open API was created with similar goals in mind. This API eliminates the need for applications developers to integrate vendor-specific or proprietary APIs to access high-quality entropy. Instead, it allows application developers to retrieve entropy from one or more sources using a single common API. Developers can adapt to changes in their QRNG requirements without additional development effort, reducing the risk of vendor lock-in and future rework, while encouraging the use of superior entropy for cryptographic and other applications.

This API is agnostic to the deployment model of the QRNG, as long as it provides a REST API interface. This allows developers to integrate a QRNG into their applications across a wide range of environments, including deployments within their local datacenter, applications in cloud environments, or edge computing environments such as IoT. This flexibility ensures broad coverage to ensure high-quality entropy available wherever it’s necessary.

Although the QRNG Open API was created for obtaining entropy from any QRNG platform supporting the API, it is applicable to any type of entropy delivery over REST and can be used for QRNG, TRNG, and even PRNGs. 


**Features**
REST API that is simple and easy to deploy.
POST command is used to fetch the entropy.
Vendor extensions are supported to provide flexibility for unique capabilities outside of the QRNG Open API specification.
The Open API specification doesn’t specify how the communication channel is secured as it is outside the scope.  As an example, communications between the requestor and QRNG platform can be secured with industry standard protocols such as TLS. 
Mutual authentication (mTLS) can also be used to enhance security between the provider and the requestor. 
Token authentication using the Bearer mechanism or the X-API-KEY is supported in the QRNG Open API specification and can also be used to authenticate each transaction.

**Deployment Examples**

**On-Prem Data Center Deployment**
A local data center deployment uses one or more QRNG sources that support the QRNG Open API and security devices, such as NGFWs, can make API calls to one or more QRNG sources to obtain high quality entropy for its cryptographic functions.  The QRNG components are secured using both network and TLS security


