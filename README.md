# Test Meli mutants

## Required
* Java 1.8 
* Dockers
* Maven

## Use

Run database:

* docker run -d -p 27017:27017 --name melidb mongo:latest

Run command:
```
$ ./mvnw clean package
  or
$ mvnw clean package (windows)
```

Run app in dockers:
```
* docker build -t mutants .

* docker run -p 8080:8080 --name mutants-1.0 --link melidb:mongo -d mutants

```