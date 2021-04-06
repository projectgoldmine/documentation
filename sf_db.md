
# SalesFroce database schema

![sf db](https://raw.githubusercontent.com/projectgoldmine/documentation/main/sf_erd.png)



## 1) salesforce_instance table

 stores data  connected salesforce account Data
 
  
  Column               | Description
-------------          | -------------
salesforce_instance_id | Primary ID
organization_id        | Organization ID
environment            | is the conncted account a [sandbox](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/apex_intro_get_dev_account.htm) or production account
sf_client_secret       | salesfroce connected app [client secret](https://docs.datawatch.com/swarm/desktop/Generating_a_Client_ID_and_ClientSecret_Key_for_Salesforce_Connections.htm)
sf_refresh_token       | salesforce refreach token. only used for batch import
sf_organization_id     | salesforce [organization ID](https://help.salesforce.com/articleView?id=000325251&type=1&mode=1) 


## 2) salesforce_login table

In Salesforce users can have different levels of access. This table  stores salesforce data related for each user 

 Column            | Description
-------------      | -------------
sf_user_id         |  user salesforce ID
sf_id              |  user salesforce rest api url to get user data
sf_access_token    |  user access token 
sf_instance_url    |  user salesforce account [user link](https://help.salesforce.com/articleView?id=000322728&type=1&mode=1). 
sf_partner_url     |  user account SOAP url. not in use. we use REST

## 3) salesforce_dataflow_map table

This table saves data flow data on the visualizer type version. Each version can have multiple mappings with different SalesForce objects  


 Column                        | Description
-------------                  | -------------
salesforce_dataflow_map_id     |  Primary ID
salesforce_instance_id         |  salesforce Instance ID
visualizer_type_version_id     |  visualizer type version id
name                           |  mapping name
primary                        |  is it a primary mapping. there can be more than one mapping but only one can be primary
auto_save                      |  should save data to salesForce automatically, work for vroi old UI but implemented in common UI   


## 4) salesforce_dataflow_item table
This table saves  SalesForce objects mapped. 



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_item_id    | Primary ID
salesforce_dataflow_map_id     |  salesforce_dataflow_map_id
enable_save                    |  save this field to salefroce 
lock_save                      |  not in use
enable_load                    |  load field data from salesforce into VROI VT
unlink                         |  can this field be unlinked
unlink_value                   |  the value set when visualizer is unliked from Salesforce



## 5) salesforce_dataflow_inclusion table

Multiple salesforce objects can be mapped in a single mapping. This is just an associated table to hold 1 to multiple relation 



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_id         |  salesforce dataflow id
salesforce_dataflow_item_id    |   salesforce dataflow item id


## 6) salesforce_dataflow_sobject table

Saves variable types mapped with salesforce fields 


 Column                                       | Description
-------------                                 | -------------
salesforce_dataflow_sobject_id                | Primary ID
salesforce_dataflow_map_id                    | salesforce dataflow map id
sf_name                                       | Fields SF name
sf_label                                      | Field SF label
referencing_salesforce_dataflow_sobject_id    | Salesforce object id
sf_reference_field_name                       | SF field API name
sf_reference_name                             | not in use



## 7) salesforce_dataflow_sobject_field table



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_item_i     | 
salesforce_dataflow_sobject_id |  
sf_name                        |   
sf_label                       |  


## 8) salesforce_dataflow table



 Column                        | Description
-------------                  | -------------
salesforce_dataflow_id         | 
salesforce_dataflow_map_id     |  
visualizer_id                  |   
created                        |  
direction                      |  
sf_object_id                   |
