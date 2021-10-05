# Code 401 - Reading Notes
<!-- All references used were from Code 401 reading
assignment 09-->
## WRRC
### Step 1: Local Processing

`<protocol>://<host><:optional port>/<path/to/resource><?query>`

`|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|`
### Step 2: Resolve an IP
### Step 3: Establish a TCP Connection
### Step 4: Send an HTTP Request
### Step 5: Tearing Down and Cleaning Up

## Java and WRRC
- Performing an HTTP requests in Java with the built-in Java class HttpUrlConnection.
- HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that we need are part of the java.net package
- Use `openConnection()`
```java
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```
- Adding headers to a request can be achieved by using the setRequestProperty() method:

```Java
con.setRequestProperty("Content-Type", "application/json");
``` 
To read the value of a header from a connection, we can use the getHeaderField() method:
```java
String contentType = con.getHeaderField("Content-Type");
```


[BACK TO HOME](../README.md)
