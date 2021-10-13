# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 18 -->
[comment]: <> (https://www.baeldung.com/hibernate-many-to-many)
[comment]: <> (https://scholar.harvard.edu/files/mickens/files/thisworldofours.pdf)

## Web App Security
### @ManyToMany Annotation
![ManyToMany](../New.webp)

In this scenario, any given employee can be assigned to multiple projects and a project may have multiple employees working for it, leading to a many-to-many association between the two.

We have an employee table with employee_id as its primary key and a project table with project_id as its primary key. A join table employee_project is required here to connect both sides.

The model classes Employee and Project need to be created with JPA annotations:

@Entity
@Table(name = "Employee")
public class Employee {
```java
@Entity
@Table(name = "Employee")
public class Employee {
    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
    name = "Employee_Project", 
    joinColumns = { @JoinColumn(name = "employee_id") }, 
    inverseJoinColumns = { @JoinColumn(name = "project_id") }
    )
    Set<Project> projects = new HashSet<>();
    // standard constructor/getters/setters
}

@Entity
@Table(name = "Project")
public class Project {
        @ManyToMany(mappedBy = "projects")
        private Set<Employee> employees = new HashSet<>();
        // standard constructors/getters/setters   
}
```

[BACK TO HOME](../README.md)
