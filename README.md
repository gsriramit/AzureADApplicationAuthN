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

## Migration from legacy authentication methods 

### Migration of application authentication from ADFS to AAD
1. Sample application and the sequence of steps in completing the migration of authN- https://github.com/Azure-Samples/ms-identity-dotnet-adfs-to-aad
2. [White paper](Migration/ADFSToAzureAD/MigratingApplicationAuthenticationtoAzureActiveDirectory.pdf) detailing a systematic approach to migtating apps that use ADFS for authN to modern authN and authZ using Azure AD

### Migration using the "Staged Rollout" Method
1. Migrate to cloud authN using staged rollout - https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-staged-rollout
2. Migrate from Federated to cloud authN using staged rollout- https://docs.microsoft.com/en-us/azure/active-directory/hybrid/migrate-from-federation-to-cloud-authentication#staged-rollout
3. Testing a staged rollout - https://mslearn.cloudguides.com/en-us/guides/Test migration to cloud authentication using staged rollout in Azure AD
4. How to implement staged rollout (Video reference) - https://www.youtube.com/watch?v=LFTE1epYDFQ&ab_channel=MicrosoftAzure

## Support for Legacy Authentication Methods (from Azure AD in a hybrid setup)
1. AzureAD Application Proxy working & event flow diagram- https://docs.microsoft.com/en-us/azure/active-directory/app-proxy/application-proxy#how-application-proxy-works
2. Integration with Network and Application Delivery Controller Vendors(ADC)
   - Akamai Enterprise Application Access- https://www.youtube.com/watch?v=QlLsw-1LfKs&ab_channel=AkamaiTechnologies
   - Secure Hybrid Access Features- https://azure.microsoft.com/en-us/services/active-directory/sso/secure-hybrid-access/#features
   - Steps to integrate Azure AD (for authentication) with apps that are managed by Akamai (apps that use legacy authentication) -https://docs.microsoft.com/en-us/azure/active-directory/saas-apps/akamai-tutorial

### High-Level Architecture Diagram
![image](https://user-images.githubusercontent.com/13979783/160269354-cb842013-ffad-4def-a2b8-98919ba1c8f1.png)


## SaaS
### Saas Applications Integration and Setup
1. Integrating Applications with Azure Active Directory (Including the configuration of SSO)- https://www.youtube.com/watch?v=a3OOzqEh_Zw&list=PLQL1JGGe-t0tfWbaGzQYdUfRRmc6-CSMz&index=6&ab_channel=MicrosoftAzure
2. Planning a SSO deployment- https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/plan-sso-deployment#single-sign-on-options


## Multitenant Applications
1. Multi-tenant architecture for SaaS apps with Microsoft 365 and Azure Active Directory- https://www.youtube.com/watch?v=RjGVOFm39j0&t=2s
2. Azure AD Cross-Tenant Access Settings Deep Dive - https://www.youtube.com/watch?v=Ku64fo7iZ4Y&list=PLQL1JGGe-t0tfWbaGzQYdUfRRmc6-CSMz&index=22&ab_channel=JohnSavill%27sTechnicalTraining
   - Architecture Diagram - TBD

