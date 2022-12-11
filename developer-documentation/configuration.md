---
description: Registry provides following configuration properties
---

# Configuration

| Properties                                   | Description                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| notification\_enabled                        | boolean value which determines whether notification is to be sent or not                                                                                                                                                                                                                                                                       |
| notification\_url                            | url which will be used to send notification url                                                                                                                                                                                                                                                                                                |
| registry\_perRequest\_indexCreation\_enabled | boolean value which determines if index needs to be created at database level                                                                                                                                                                                                                                                                  |
| external\_entities                           | comma separated strings of external entities                                                                                                                                                                                                                                                                                                   |
| workflow**.**enable                          | boolean value to enable or disable the workflow i.e attestation policy                                                                                                                                                                                                                                                                         |
| async\_enabled                               | create entities asynchronously                                                                                                                                                                                                                                                                                                                 |
| kafka\_create\_entity\_topic                 | if async\_enabled, then this property defines the topic name to which new async requests are pushed                                                                                                                                                                                                                                            |
| kafka\_post\_create\_entity\_topic           | if async is enabled, then this property defines the topic name to which the response of create-entity is pushed                                                                                                                                                                                                                                |
| search\_offset                               | this is the default offset that will be used while searching,                                                                                                                                                                                                                                                                                  |
| search\_limit                                | this is the default limit that will be used or the max value that can be used to as a limit in the search                                                                                                                                                                                                                                      |
| search\_expandInternal                       | boolean value, if set true, all the search results will be expanded to include internal objects.                                                                                                                                                                                                                                               |
| database\_provider                           | this property states which database is to be used. Providers available are NEO4J, SQLG, CASSANDRA, ORIENTDB, TINKERGRAPH (in-memory)                                                                                                                                                                                                           |
| connectionInfo\_uri                          | url to connect to database. eg Postgres - jdbc:postgresql://localhost:5432/yourdb                                                                                                                                                                                                                                                              |
| connectionInfo\_username                     | username to be used to connect to database                                                                                                                                                                                                                                                                                                     |
| connectionInfo\_password                     | password to be used to connect to database                                                                                                                                                                                                                                                                                                     |
| connectionInfo\_maxPoolSize                  | Database connection pool size                                                                                                                                                                                                                                                                                                                  |
| verify\_url                                  | this url will be used to verify the issued VC. point it to {certification\_signer}/verify                                                                                                                                                                                                                                                      |
| certificate\_health\_check\_url              | certificate api service's health check url                                                                                                                                                                                                                                                                                                     |
| template\_folder\_path                       | path from which default template will be loaded if no external template is provided. File name should be the **`name_of_schema.appropriate_extention`** The location should be in resources folder                                                                                                                                             |
| audit\_enabled                               | This audit configuration will enable audit logging in the system                                                                                                                                                                                                                                                                               |
| audit\_frame\_store                          | <p>FILE : Store the audit log in files. <br>DATABASE : Store the audit log in primary database configured in database properties <br>ELASTIC : Store the audit log in elastic search configured in elastic properties.</p>                                                                                                                     |
| audit\_suffix                                | suffix which is used for schema name to store audit information for a particular entity type                                                                                                                                                                                                                                                   |
| audit\_suffixSeparator                       | separator between entity name and audit\_suffix                                                                                                                                                                                                                                                                                                |
| keycloack\_user\_email\_actions              | email actions which will be trigger by keycloak example email actions: VERIFY\_EMAIL, UPDATE\_PROFILE, UPDATE\_PASSWORD,TERMS\_AND\_CONDITIONS etc. email details should be configured in keycloak realm settings                                                                                                                              |
| validation\_enabled                          | boolean property to check for request body to be validated in specific format                                                                                                                                                                                                                                                                  |
| validation\_type                             | type in which request body needs to be validated. eg JSON                                                                                                                                                                                                                                                                                      |
| service\_connection\_timeout                 | Set the connection timeout in milliseconds for the underlying request configuration                                                                                                                                                                                                                                                            |
| service\_connection\_request\_timeout        | Set the timeout in milliseconds used when requesting a connection from the connection manager using the underlying request Configuration                                                                                                                                                                                                       |
| service\_read\_timeout                       | Set the socket read timeout in milliseconds for the underlying request configuration                                                                                                                                                                                                                                                           |
| http\_max\_connections                       | maximum http connections                                                                                                                                                                                                                                                                                                                       |
| taskExecutor\_index\_threadPoolName          | Specify the prefix to use for the names of newly created threads.                                                                                                                                                                                                                                                                              |
| taskExecutor\_index\_corePoolSize            | Set the ThreadPoolExecutor's core pool size.                                                                                                                                                                                                                                                                                                   |
| taskExecutor\_index\_maxPoolSize             | Set the ThreadPoolExecutor's maximum pool size.                                                                                                                                                                                                                                                                                                |
| taskExecutor\_index\_queueCapacity           | Set the capacity for the ThreadPoolExecutor's BlockingQueue.                                                                                                                                                                                                                                                                                   |
| auditTaskExecutor\_threadPoolName            | Specify the prefix to use for the names of newly created threads.                                                                                                                                                                                                                                                                              |
| auditTaskExecutor\_corePoolSize              | Set the ThreadPoolExecutor's core pool size.                                                                                                                                                                                                                                                                                                   |
| auditTaskExecutor\_maxPoolSize               | Set the ThreadPoolExecutor's maximum pool size.                                                                                                                                                                                                                                                                                                |
| auditTaskExecutor\_queueCapacity             | Set the capacity for the ThreadPoolExecutor's BlockingQueue.                                                                                                                                                                                                                                                                                   |
| elastic\_search\_connection\_url             | url for elastic search connection if elastic search is enabled. Elastic search is enabled using search\_providerName                                                                                                                                                                                                                           |
| search\_providerName                         | The search mechanism to use. Values could be either NativeSearchService or ElasticSearchService. If NativeSearchService, then every search API uses the same database as the writes. May not offer high speed reads. This is the default search service, if this config is not provided. If ElasticSearchService, then Elastic search is used. |
| sunbird\_sso\_realm                          | keycloak realm name to be used for authentication and authorization                                                                                                                                                                                                                                                                            |
| sunbird\_sso\_url                            | keycloak connection url                                                                                                                                                                                                                                                                                                                        |
| sunbird\_sso\_admin\_client\_id              | client id to be used as admin                                                                                                                                                                                                                                                                                                                  |
| sunbird\_sso\_admin\_client\_secret          | secret key of keycloak admin client set by using sunbird\_sso\_admin\_client\_id                                                                                                                                                                                                                                                               |
| claims\_url                                  | url in order to connect to claims service                                                                                                                                                                                                                                                                                                      |
| sign\_url                                    | url in order to connect to certificate signer to sign the document                                                                                                                                                                                                                                                                             |
| sign\_health\_check\_url                     | certificate signer health check url                                                                                                                                                                                                                                                                                                            |
| signature\_enabled                           | boolean value which determines whether signature is to be created for a document                                                                                                                                                                                                                                                               |
| pdf\_url                                     | url to fetch certificate from certificate api service                                                                                                                                                                                                                                                                                          |
| certificate\_health\_check\_url              | certificate api health check url                                                                                                                                                                                                                                                                                                               |
| template\_base\_url                          | api endpoint to get default templates stored in sunbird-rc                                                                                                                                                                                                                                                                                     |
| sunbird\_keycloak\_user\_set\_password       | boolean value to default password for user/owner of entity in keycloak                                                                                                                                                                                                                                                                         |
| filestorage\_connection\_url                 | minio connection url to store files                                                                                                                                                                                                                                                                                                            |
| filestorage\_access\_key                     | access key of minio                                                                                                                                                                                                                                                                                                                            |
| filestorage\_secret\_key                     | secret key of minio                                                                                                                                                                                                                                                                                                                            |
| filestorage\_bucket\_key                     | bucket name where to store the files in minio                                                                                                                                                                                                                                                                                                  |
| registry\_base\_apis\_enable                 | if enabled the exisitng /add /update apis will be enabled. This is to enable backward compatibility                                                                                                                                                                                                                                            |
| sunbird\_keycloak\_user\_password            | if sunbird\_keycloak\_user\_set\_password is set to true, provide this value to set this as default user password                                                                                                                                                                                                                              |
| logging.level.root                           | <p>The log level that will be used for logging. Default logging is INFO. <br>Values supported:<br>INFO<br>DEBUG<br>WARN<br>ERROR</p>                                                                                                                                                                                                           |
| enable\_external\_templates                  | boolean value which when set to true, one can retrieve the certificate pdf using external templates                                                                                                                                                                                                                                            |
| authentication\_enabled                      | boolean value to enable authentication in the system                                                                                                                                                                                                                                                                                           |
| kafka\_bootstrap\_address                    | url for kafka connection                                                                                                                                                                                                                                                                                                                       |
| webhook\_enabled                             | boolean value to enable webhook if async\_enabled is true                                                                                                                                                                                                                                                                                      |
| webhook\_url                                 | if async\_enabled and webhook\_enabled is set to true, the caller can retrieve information of the created entity once it is generated via this webhook url                                                                                                                                                                                     |
| redis\_host                                  | redis connection url                                                                                                                                                                                                                                                                                                                           |
| redis\_port                                  | port on which redis is running                                                                                                                                                                                                                                                                                                                 |
| manager\_type                                | if using a single instance of registry, set this value to DefinitionsManager else set to DistributedDefinitionsManager                                                                                                                                                                                                                         |
| service\_retry\_maxAttempts                  | The number of times an attempt must be made to reach to the service                                                                                                                                                                                                                                                                            |
| service\_retry\_backoff\_delay               | The fixed time interval, in milliseconds, between each such attempt.                                                                                                                                                                                                                                                                           |

### Claims Service

| Properties     | Description                                                                                                   |
| -------------- | ------------------------------------------------------------------------------------------------------------- |
| sunbirdrc\_url | used by claim service to communicate with sunbirdrc. url which corresponds to registry deployed host and port |

### Certificate Api service

<table><thead><tr><th>Properties</th><th>Description</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>CUSTOM_TEMPLATE_DELIMITERS</td><td>Delimeters to be used to parse credential/certificate template. By default <code>{{,}}</code></td><td></td><td></td></tr><tr><td>QR_TYPE</td><td>Types of QR codes that sunbird supports<br>1. W3C-VC<br>2. URL-W3C-VC (if VC needs to be sent as a URL)<br>3. URL (If only a URL needs to be part of the QR. The URL will only contain the entity name and osid. </td><td></td><td></td></tr><tr><td>CERTIFICATE_DOMAIN_URL</td><td>Base URL to be used when <code>QR_TYPE</code> is URL*</td><td></td><td></td></tr></tbody></table>

### Certificate signer service

<table><thead><tr><th>Properties</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>CACHE_CONTEXT_URLS</td><td>Predefine a set of context urls to be cached to avoid runtime network access.</td><td></td></tr><tr><td>CONFIG_BASE_PATH</td><td>path to config.json file where all the signing keys are stored</td><td></td></tr><tr><td>CUSTOM_TEMPLATE_DELIMITERS</td><td>Delimeters to be used to parse credential/certificate template. By default <code>{{,}}</code></td><td></td></tr></tbody></table>

### Notification Service

| Properties                                                                  | Description                                                                               |
| --------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| KAFKA\_BOOTSTRAP\_SERVERS in environment variable or kafka.bootstrapServers | host along with port if port is different than default i.e 9092 on which kafka is present |
| kafka.notifyTopic                                                           | topic name which holds notification messages                                              |
| smsapi.url                                                                  | api url to send sms to provided mobile numbers                                            |
| smsapi.authKey                                                              | authorization key for sms api url                                                         |
| smsapi.enable                                                               | flag to enable sending sms using sms api                                                  |
| smsapi.requestTemplate                                                      | message template to be sent to mobile number in notification message                      |
| emailsmtp.fromAddress                                                       | senders email address from which to send email                                            |
| emailsmtp.password                                                          | password for that email address                                                           |
| emailsmtp.enable                                                            | flag to enable sending email using email api                                              |
| TRACK\_NOTIFICATIONS in environment variable                                | boolean value to track all sent notifications and fetch them if needed                    |
