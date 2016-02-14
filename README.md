# phonebook-service

* This is a sample Spring Boot microservice (application).
* Phonebook microservice exposes phonebook entries and other phonebook management functionalities.

## REST example queries

* Get all entries, e.g.

```
    curl -X GET "http://localhost:8080/entries"
```


* Get entry with id=1, e.g.

```
    curl -X GET "http://localhost:8080/entries/1"
```


* Create a new entry, e.g.

```
    curl -X POST -H "Content-Type: application/json" -d '{
        "name": "Neven",
        "number": "416-555-1111",
        "type": "Mobile",
        "notes": "N/A"
    }' "http://localhost:8080/entries"
```

* Search for entries, e.g.

```
    curl -X GET "http://localhost:8080/entries/search/by-name?name=Jane"
    curl -X GET "http://localhost:8080/entries/search/by-name-ignore-case?name=jane"
    curl -X GET "http://localhost:8080/entries/search/by-partial-name?name=Ja%25"
    curl -X GET "http://localhost:8080/entries/search/by-partial-name-ignore-case?name=ja%25"
```

## Spring Boot Actuator

The Spring Boot Actuator provides useful insights into Spring Boot application, e.g. [http://localhost:8080/actuator] (http://localhost:8080/actuator)

* General information about application, e.g. [http://localhost:8080/info] (http://localhost:8080/info)
* Collected counters and metrics, e.g. [http://localhost:8080/metrics] (http://localhost:8080/metrics)
* Tracing information, e.g. [http://localhost:8080/trace] (http://localhost:8080/trace)
* Thread dump, e.g. [http://localhost:8080/dump] (http://localhost:8080/dump)
* Environment variables, e.g. [http://localhost:8080/env] (http://localhost:8080/env)
* Health indicators, e.g. [http://localhost:8080/health] (http://localhost:8080/health)
* URL mappings, e.g. [http://localhost:8080/mappings] (http://localhost:8080/mappings)
* Spring Beans, e.g. [http://localhost:8080/beans] (http://localhost:8080/beans)


