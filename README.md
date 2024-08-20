# Tokyo-Olympics-Data-Pipeline-on-Azure
Data engineering project that builds and manages a scalable data pipeline for the Tokyo Olympics using Azure services, including data ingestion, transformation, and storage.


configs = {
    "fs.azure.account.auth.type": "OAuth", 
    "fs.azure.account.oauth.provider.type": "org.apache.hadoop.fs.azurebfs.oauth2.ClientCredsTokenProvider",
    "fs.azure.account.oauth2.client.id": dbutils.secrets.get(scope = "<scope-name>", key = "client-id"),
    "fs.azure.account.oauth2.client.secret": dbutils.secrets.get(scope = "<scope-name>", key = "client-secret"),
    "fs.azure.account.oauth2.client.endpoint": "https://login.microsoftonline.com/" + dbutils.secrets.get(scope = "<scope-name>", key = "tenant-id") + "/oauth2/token"
}
