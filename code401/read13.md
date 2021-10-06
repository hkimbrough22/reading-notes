# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 13 -->
[comment]: <> (https://www.baeldung.com/spring-data-rest-relationships)

[comment]: <> (https://www.baeldung.com/integration-testing-in-spring)
## Related Resources and Integration Testing

### Resources
- `@OneToOne` = Library to Address
- `OneToMany` = Library to Book
- `ManyToMany` = Author to Book

All need a repository and instance.
Then create an association.

### Testing
- JUnit 5 defines an extension interface through which classes can integrate with the JUnit test.

- We can enable this extension by adding the @ExtendWith annotation to our test classes and specifying the extension class to load. To run the Spring test, we use `SpringExtension.class`.

- We also need the `@ContextConfiguration` annotation to load the context configuration and bootstrap the context that our test will use.
```java

@ExtendWith(SpringExtension.class)
@ContextConfiguration(classes = { ApplicationConfig.class })
@WebAppConfiguration
public class GreetControllerIntegrationTest {
....
}
```
- Notice how, in @ContextConfiguration, we provide the ApplicationConfig.class config class, which loads the configuration we need for this particular test.



[BACK TO HOME](../README.md)