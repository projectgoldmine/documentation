
# SalesFroce database schema

![sf db](https://raw.githubusercontent.com/projectgoldmine/documentation/main/sf_erd.png)



## salesforce_instance table

 stores data  connected salesforce account Data
 
  
  Column           | Description
-------------      | -------------
environment        | is the conncted account a sandbox or production account
sf_client_secret   |  salesfroce connected app client secret
sf_refresh_token   | salesforce refreach token. only used for batch import
sf_organization_id | salesforce organization ID 


## salesforce_login table

 Column            | Description
-------------      | -------------
sf_user_id         | 
sf_id              |  
sf_access_token    | 
sf_instance_url    | 
sf_partner_url     |
