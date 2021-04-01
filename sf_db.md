
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

In Salesforce users can have differentlevels of access. This table  stores salesforce data related for each user 

 Column            | Description
-------------      | -------------
sf_user_id         |  user salesforce ID
sf_id              |  user salesforce rest api url to get user data
sf_access_token    |  user access token 
sf_instance_url    |  user salesforce account user. 
sf_partner_url     |  user account SOAP url. not in use. we use REST

## salesforce_dataflow_map table



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_map_id     | 
salesforce_instance_id         |  
visualizer_type_version_id     |   
name                           |  
primary                        |  
auto_save                      |


## salesforce_dataflow_item table



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_item_id    | 
salesforce_dataflow_map_id     |  
enable_save                    |   
lock_save                      |  
enable_load                    |  
unlink                         |
unlink_value                   |
if_sf_value                    |
set_to                         |


## salesforce_dataflow_inclusion table



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_id         | 
salesforce_dataflow_item_id    |  


## salesforce_dataflow_sobject table



 Column                                       | Description
-------------                                 | -------------
salesforce_dataflow_sobject_id                | 
salesforce_dataflow_map_id                    |  
sf_name                                       |   
sf_label                                      |  
referencing_salesforce_dataflow_sobject_id    |  
sf_reference_field_name                       |
sf_reference_name                             |
sf_usage_field_name                           |
sf_usage_field_label                          |





## salesforce_dataflow table



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_id         | 
salesforce_dataflow_map_id     |  
visualizer_id                  |   
created                        |  
direction                      |  
sf_object_id                   |
