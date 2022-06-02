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
    
   ```json{
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
    }``` 
    
#### Put a document to twitter index as follows

https://localhost:9200/twitter/_doc/1

```{
    "name": "Radhe Shyam",
    "sex": false,
    "age": 21,
    "password": "U29tZSBiaW5hcnkgYmxvYg==",
    "phone_number": "9999161236",
    "old": "YES",
    "salary": 200.2,
    "createdOn": "2022-02-02"
}```

