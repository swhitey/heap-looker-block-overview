**Heap Looker Block**

Heap Connect provides direct SQL access to your retroactive Heap data, automatically managed in Redshift. The Heap Looker block provides a starting point for Heap data exploration in Looker, specifically for Heap's Redshift, Bigquery, and Snowflake offering.


# Implementation Instructions
1. Download the looker block from here
2. Drag and drop files into a blank Look ML project
3. Modify the connection in the heap_block model file to reflect the name of your warehouse connection


## Optional Customization:



### Add User Property Drill Downs
1. In the users file add additional dimensions to the user view based off the column names of the properties.
2. Add a filter for the given paremeter to the lookML Dashboard:
  
``` name: property_name
    type: field_filter
    explore: sessions
    field: users.property_name
```


### Add Custom Channel Mappings
1. in the sessions view edit the dimension referrer mapping with additional case when statements
