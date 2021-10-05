# Code 401 - Reading Notes
<!-- All references used were from Code 401 reading
assignment 12-->
[comment]: <> (https://www.baeldung.com/spring-requestmapping)

[comment]: <> (https://spring.io/guides/gs/accessing-data-jpa/)

[comment]: <> (https://www.baeldung.com/spring-data-repositories)
## Spring RESTful Routing & Static Files
Spring MVC: @RequestMapping.
Simply put, the annotation is used to map web requests to Spring Controller methods

```java
  @RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
  @ResponseBody
  public String getFoosBySimplePath() {
  return "Get some Foos";
  }
```
  To test out this mapping with a simple curl command, run:

`curl -i http://localhost:8080/spring-rest/ex/foos`

The mapping can be narrowed even further by specifying a header for the request:

`@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)`

`curl -i -H "key:val" http://localhost:8080/spring-rest/ex/foos`

Multiple headers:

`  headers = { "key1=val1", "key2=val2" }, method = GET)
`

`curl -i -H "key1:val1" -H "key2:val2" http://localhost:8080/spring-rest/ex/foos
`


[BACK TO HOME](../README.md)