## About SALT

The Situational Awareness and Learning Tool (SALT) is a cloud-based tool that enables sharing and rapid coordination of analytics and situational awareness to protect the health, wellbeing, and security of Hamilton County residents in current and future pandemics. SALT rapidly and flexibly supports collaboration, data analysis, and communications with and between stakeholders at appropriate levels of security and access. Stakeholder data must be handled appropriately and safeguarded according to owner intent and statutory and data use agreement needs. To ensure this, the data governance policies and processes outlined here will govern how data are collected, used, and managed in SALT.

## Data Usage

SALT does not store sensitive, individually-identifying data (e.g. HIPAA-defined Protected Health Information), but rather reads it "just in time" for production of data analysis products.

While SALT has the capability to connect with other data systems (e.g., an SFTP server hosted by an HIE, American Community Survey Data, Cincinnati Open Data Portal, Epic COSMOS), SALT is a platform for *virtually assembling data* and *sharing data analysis products* (e.g., an interactive dashboard of recent, weekly COVID-19 hospital admissions by ZIP code). 
“Virtually assembling” data means that data are not permanently stored or hosted within SALT; rather, the data analysis products are created from source code that read data temporarily into computer memory to execute data analyses and generate the associated products. 

Avoiding the copying and storing of sensitive data from sources drastically reduces the potential risks of unintentionally exposing sensitive data to those who are not authorized to view or use them.

## Data Access

Because SALT uses extant data, use of those data are subject to any data-specific use agreements or legal restrictions regarding those data. 
For example, if a researcher wishes to generate a dashboard using data from an electronic health record or records, then the data and resulting data analysis products will be subject to the governance specified in the corresponding IRB protocol or Epic user agreements. 
As another example, if data are subject to Data Use Agreements, the terms of the DUAs will govern the use of data and control of derived analytic products in SALT. 
If data are freely available and in the public domain (e.g. Creative Commons Zero license), analytic products will similarly be in the public domain. 

When questions arise regarding combining open available data into potentially sensitive analytic products, the SALT Governance Panel will be consulted.  

## SALT Users

SALT users are on boarded by requesting a new SALT account through a [sign up form](https://redcap.link/salt_use_agreement) and creation of a user account by a SALT administrator.

Operationally, SALT has “publisher” accounts and “viewer” accounts. 
Publishers are individuals with the credentials and permissions to publish data analysis products to SALT and control who has access to the data analysis products.
Viewer account holders have permission to view and interact with specific data analysis products. 

### Authentication

Account authentication is federated, such that users create a SALT account using their existing organizational credentials. Organizational email addresses will be used as a unique identifier to maintain a list of authenticated SALT user accounts.

### Authorization 

Authenticated SALT users' unique identifiers are used to set access permissions individually for each data analysis product by SALT publishers.

## Auditing Safe and Secure Usage of SALT

All interactions with SALT, including by “publishers,” “viewers,” and system administrators, are logged and stored in a separate location and retained for any line-level auditing of SALT activity. Such logging data may also be used to understand and characterize how users interact with SALT, in order to improve the platform.

Intermediate data products, such as aggregations of other data, can be stored on SALT and will continually be audited by SALT administrators to ensure no storage of individual-level or private data.



