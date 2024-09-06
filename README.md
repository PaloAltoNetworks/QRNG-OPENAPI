# QRNG-OPENAPI
GitHub Repository for QRNG Open API


**Readme**
The QRNG Open API was created by Palo Alto Networks and six technical partners (Anametric, ID Quantique, Qrypt, Quantinuum, Quantropi, and Quside) to simplify the ability to obtain high quality entropy from an external QRNG platform (source).  The QRNG Open API provides a common mechanism to obtain information on the QRNG platform’s capabilities, retrieve entropy from the platform, and to check the health of the entropy provided.  

The QRNG Open API removes the need to implement a specific vendor SDK or API and allows one or more entropy sources to be implemented with just one common API.  This eliminates the need to change a specific vendor’s communication mechanism if the QRNG requirement changes and greatly simplifies the implementation while reducing risk of rework in the future.

Although the open API was created for obtaining entropy from a QRNG platform, it is applicable to any type of entropy delivery over REST and can be used for QRNG, TRNG, and even PRNGs.


**Features**
- REST API is simple and easy to deploy.
- POST command is used to fetch the entropy.
- Vendor extensions are supported to provide flexibility for unique capabilities outside of the QRNG Open API specification.
- Communications between the requestor and QRNG platform can be secured with industry standard protocols such as TLS, VPN, etc. Certificate authentication can also be used to enhance security 
  between the provider and the requestor. The Open API specification doesn’t specify how the communication channel is secured as it is outside the scope.
- Token authentication using the Bearer mechanism or the X-API-KEY is supported in the QRNG Open API specification.
