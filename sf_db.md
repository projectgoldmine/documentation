
# SalesFroce database schema

![sf db](https://raw.githubusercontent.com/projectgoldmine/documentation/main/sf_erd.png)



## salesforce_instance table

 stores data of connected salesforce account with VROI
 
 
  environment	tinyint	:  is the conncted account a sandbox or production account
  sf_client_id	varchar(255)	: salesfroce connected app client ID
  sf_client_secret	blob	: salesfroce connected app client secret
  sf_refresh_token	longtext :  salesforce refreach token. only used for batch import
  sf_organization_id	varchar(255)	:  salesforce organization ID


