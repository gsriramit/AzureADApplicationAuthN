# Introduction
This repository contains a collection of resources that explain the cloud-native &amp; hybrid identities and the different authN methods for application access

## Authentication Methods for Hybrid Identity
**Pass-through Authentication (PTA)**  
How does PTA work(with architecture diagram)- https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-how-it-works  

### Password Hash-Sync
How does PHS work - https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization

### Federation
1. What is Federation - https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-fed  
2. How does Federation work- https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-fed-whatis  
3. Customizing Azure AD Connect Settings to configure federation with Windows ADFS - https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-custom#configuring-federation-with-ad-fs  
4. Customizing Azure AD Connect Settings to configure federation with Ping Federate- https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-custom#configuring-federation-with-pingfederate  
5. Deploying ADFS Servers on Azure (with Web Application Proxy for external access) - https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/how-to-connect-fed-azure-adfs
6. Additional Architecture Diagrams
   - [ADFS Setup](ArchitectureDiagrams/On-PremiseADFSAuthN-Setup.png)
   - [ADFS Cross-Domain Access](ArchitectureDiagrams/On-PremiseADFS-CrossDomainAccess-AuthN.png)

### Authentication Options in AAD- Whitepaper
[White Paper](IdentityAuthenticationOptions-WhitePaper/IdentityAuthenticationOptions.pdf) with the different authentication options in AAD with the corresponding architecture diagrams & the decision tree to use to identify the best-suited option- 
1. Cloud authentication
   - Cloud-Only (Azure AD only identities)
   - Password Hash-Sync + Seamless SSO 
   - Passthrough Authentication + Seamless SSO
2. Federated AUthentication
   - ADFS (Active Directory Federation Services)
   - Third-Party Federation Services (Ping, Okta, Auth0 etc.,)

### Migration of application authentication from ADFS to AAD
Sample application and the sequence of steps in completing the migration of authN- https://github.com/Azure-Samples/ms-identity-dotnet-adfs-to-aad



