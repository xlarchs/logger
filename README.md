# Logger
MongoDB Logger - File Logger - Elasticsearch Logger with serilog .NET 5


## Usage
You need to edit "appsettings.json" before start the project.

 
 - ElasticSearch Config
  ```c#
"ElasticSearchConfig": {
    "ConnectionString": "http://localhost:9200",
    "UserName": "",
    "Password": ""
  }
```

 - Mongo Database Config
  ```c#
"MongoDbSettings": {
    "CollectionName": "log",
    "ConnectionString": "mongodb://localhost:28017/logger?uuidRepresentation=Standard",
    "DatabaseName": "logger"
  }
```

 - Serilog Configurations
  ```c#
 "SeriLogConfigurations": {
    "ProjectName": "LoggerProject",
    "FileLogConfiguration": {
      "FolderPath": "C:\\Logs\\LoggerProject",
      "SeqConnectionString": "http://localhost:5341/"
    },
    "MongoDbConfiguration": {
      "ConnectionString": "mongodb://localhost:28017/logger?uuidRepresentation=Standard",
      "SeqConnectionString": "http://localhost:5341/"
    },
    "SeqConfiguration": {
      "ConnectionString": "http://localhost:5341/",
      "SeqConnectionString": "http://localhost:5341/"
    },
    "ElasticsearchConfiguration": {
      "ConnectionString": "http://localhost:9200/",
      "TemplateName": "serilog-events-template",
      "IndexFormat": "logger-{0:yyyy.MM.dd}",
      "SeqConnectionString": "http://localhost:5341/"
    }
  }
```
