# Spring Framework

spring is a meta framework, a framework of frameworks

## What is a Framework

### Vertical applications vs Horizontal applications

Vertical: specific domain

Horizontal: common to many domains

### History

- Rod Johnson, creator, 2004
Expert One-on-One J2EE Development without EJB

## Spring projects

- Spring Boot
- Spring Core
- Spring Cloud
- Spring Roo
- Spring LDAP
- Spring Web Flow
- Spring Web Services

### Spring Framework (core) 

- is a framework
- offers a container (IoC) Spring Application Context
- Components or beans
- Dependency Injection

#### Dependency Inversion Principle

- Abstractions (interfaces, abstract classess) over implementations (classes)
- you should not depend on a particular class
- interfaces are contracts

```java
public interface Database {
    ...
}

public class MySQLDb implements Database {
    ...
}

public class PostgreSQL implements Database {
    ...
}

public class ProductService {
    private Database db;
    public ProductService(Database db) {
        this.db = db;
    }
    ...
}
```

## Spring modules vs Spring Projects

module: basic spring packaging unit (Spring JDBC)

project: specific functionality uses several modules (Spring Data)

all projects and modules use at some degree Spring Core

