# elastic-search

#### Create an index twitter with two fields name and sex with their specific type

https://localhost:9200/twitter?pretty

PUT --> 
    {
        "settings": {
            "number_of_shards": 3,
            "number_of_replicas": 2
        },
        "mappings": {
            "properties": {
                "name": {
                    "type": "text"
                },
                "sex": {
                    "type": "boolean"
                }
            }
        }
    }
#### Modify an index twitter with more properties 

https://localhost:9200/twitter/_mapping

PUT -->
    
   {
        "properties": {
            "name": {
                "type": "text"
            },
            "sex": {
                "type": "boolean"
            },
            "age" : {
                "type" : "long"
            },
            "password" : {
                "type" : "binary"
            }
            ,
            "phone_number" : {
                "type" : "keyword"
            },
            "old" : {
                "type" : "constant_keyword"
            } ,
            "salary" : {
                "type" : "double"
            },
            "createdOn" : {
                "type" : "date"
            }
        }
    }

