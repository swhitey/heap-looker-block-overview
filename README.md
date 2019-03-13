# Heap Looker Blocks

This repo contains the LookML for:
1. Digital Marketing Analytics by Heap
2. User Engagement Analytics by Heap

These Heap Looker blocks provide a starting point for Heap data exploration in Looker, specifically for Heap's Redshift, Bigquery, and Snowflake offerings.

This repo is for **Redshift** if you would like to install on **BigQuery** use this repo: https://github.com/llooker/heap_block_bigquery

# Implementation Instructions
1. Download the Looker Block from here
2. Drag and drop files into a blank Look ML project
3. Modify the connection in the heap_block model file to reflect the name of your warehouse connection

Note: if you aren't querying from the `main_production` schema, you will have to update to the correct schema name in the LookML files


## Optional Customization:


### Add User Property Drill Downs
1. In the users file add additional dimensions to the user view based off the column names of the properties.
2. Add a filter for the given parameter to the lookML Dashboard:
  
``` 
    - name: property_name
    type: field_filter
    explore: sessions
    field: users.property_name
```
3. add in a key value pair under the listener for each dashboard element

### Add Custom Channel Mappings
1. in the sessions view edit the dimension referrer mapping with additional case when statements
