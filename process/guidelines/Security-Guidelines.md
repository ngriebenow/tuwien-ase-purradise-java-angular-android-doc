# Security Guidelines

## Aims
The fundamental aim of having security guidelines in place is to get closer to meeting several security properties, so that the software developed in this project can be part of system for which those properties are of significance.  Those qualities are considered throughout the development process.

### Confidentiality
This property demands that information is not available to unauthorized persons. The public is allowed to access a considerable part of the data our system handles. However, there is personal data that needs to be protected from unauthorized access -- animal shelters are no exception to data protection laws.

### Integrity
Data integrity implies that restrictions on how, under what circumstances and by whom data can be modified are enforced. Ensuring this property is of priority: Animal keepers might have to rely on the accuracy of the data in the system, as it is also a tool to communicate knowledge to colleagues, for example whether a dog tends to bite. Therefore this property is of high relevance.

### Availability
Availability requires that information is actually accessible when it is needed. A breach of this property could mean that potential adopters are lost, employees would find it to be a grave nuisance as well. There are however no legal considerations or potential dangers to keepers. Although being of relevance, for our project this one is the least important of the classic CIA properties.

## Threats

We particularly consider threats that are easy to exploit, comparatively prevalent and would have some non-negligible impact. Our prioritization is based on the assessments of [OWASP](https://owasp.org/www-project-top-ten/2017/Details_About_Risk_Factors.html). Some of the recommendations against specific threats are taken from there.

Each of the threats listed here is shown with a possible strategy to mitigate its risks. Those measures should not be seen as obligations but rather as a suggestions of how those security risks could be taken care of. Mostly it is important to understand the relevance and prevalence of these issues.


### Injections
Injections such as SQL injections are listed at the top of the [OWASP Top Ten](https://owasp.org/www-project-top-ten/) of critical security risks. In order to reduce the risk of an SQL injection, we only do parameterized queries using Prepared Statements or tools for Object Relational Mapping. Additionally, logging should provide us with valuable information in case a SQL injection has succeeded.

### Broken authentication
Attackers could gain privileges by guessing weak credentials, or using automated brute force attacks. Policies on the complexity/length of passwords can improve that. Session IDs should be invalidated after an absolute timeout or logout. On a failure there may not be any information telling whether the identifier or the credentials were incorrect, because this would enable Account Enumeration attacks. Information about authentication should be logged, particularly failed login.

### Misconfiguration
Reviewing release and security notes on components we use helps to avoid configuring an insecure system. Misconfiguration might happen on our side, but we can also help users not to end up with a configuration that enables attacks. It should be easy to newly set up a new secure system  that uses unique credentials. Ideally, there should not be any default passwords. Minimizing configuration options should also make it harder to end up with an insecure configuration. Segmenting the system enables users to configure the system in a way so that components have fewer privileges.

### Exposure of sensitive data
All data that is related to a specific user is considered sensitive; that includes credentials, data about the user and information about the relation to an animal. It would be catastrophic if an attacker could gain access to a list of plain text passwords. Therefore, all passwords should only be stored as a salted hash. Using a salted hashing function with a delay factor is necessary to turn such a scenario into one, that is not quite as alarming.

### Cross Site Scripting
There are automated tools to exploit the various forms of Cross Site Scripting. The Angular cross site scripting security model should be employed; nothings should be [explicitly trusted](https://angular.io/guide/security#bypass-security-apis).
