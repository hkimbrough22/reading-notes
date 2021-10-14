# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 19 -->
[comment]: <> (https://spring.io/guides/gs/messaging-stomp-websocket/)
## Sockets
- Spring Initializr Dependencies - Websockets
- Need to add these to dependencies
```java
implementation 'org.webjars:webjars-locator-core'
implementation 'org.webjars:sockjs-client:1.0.2'
implementation 'org.webjars:stomp-websocket:2.3.3'
implementation 'org.webjars:bootstrap:3.3.7'
implementation 'org.webjars:jquery:3.1.1-1'
```

Controller Setup
```java
@Controller
public class GreetingController {


@MessageMapping("/hello")
@SendTo("/topic/greetings")
public Greeting greeting(HelloMessage message) throws Exception {
Thread.sleep(1000); // simulated delay
return new Greeting("Hello, " + HtmlUtils.htmlEscape(message.getName()) + "!");
}

}
```

Spring Configuration
```java
@Configuration
@EnableWebSocketMessageBroker
public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {

  @Override
  public void configureMessageBroker(MessageBrokerRegistry config) {
    config.enableSimpleBroker("/topic");
    config.setApplicationDestinationPrefixes("/app");
  }

  @Override
  public void registerStompEndpoints(StompEndpointRegistry registry) {
    registry.addEndpoint("/gs-guide-websocket").withSockJS();
  }

}
```

```java

var stompClient = null;

function setConnected(connected) {
$("#connect").prop("disabled", connected);
$("#disconnect").prop("disabled", !connected);
if (connected) {
$("#conversation").show();
}
else {
$("#conversation").hide();
}
$("#greetings").html("");
}

function connect() {
var socket = new SockJS('/gs-guide-websocket');
stompClient = Stomp.over(socket);
stompClient.connect({}, function (frame) {
setConnected(true);
console.log('Connected: ' + frame);
stompClient.subscribe('/topic/greetings', function (greeting) {
showGreeting(JSON.parse(greeting.body).content);
});
});
}

function disconnect() {
if (stompClient !== null) {
stompClient.disconnect();
}
setConnected(false);
console.log("Disconnected");
}

function sendName() {
stompClient.send("/app/hello", {}, JSON.stringify({'name': $("#name").val()}));
}

function showGreeting(message) {
$("#greetings").append("<tr><td>" + message + "</td></tr>");
}

$(function () {
$("form").on('submit', function (e) {
e.preventDefault();
});
$( "#connect" ).click(function() { connect(); });
$( "#disconnect" ).click(function() { disconnect(); });
$( "#send" ).click(function() { sendName(); });
});
```
The main pieces of this JavaScript file to understand are the `connect()` and `sendName()` functions.

The connect() function uses SockJS and stomp.js to open a connection to /gs-guide-websocket, which is where our SockJS server waits for connections. Upon a successful connection, the client subscribes to the /topic/greetings destination, where the server will publish greeting messages. When a greeting is received on that destination, it will append a paragraph element to the DOM to display the greeting message.

The sendName() function retrieves the name entered by the user and uses the STOMP client to send it to the /app/hello destination (where GreetingController.greeting() will receive it).

The main.css can be omitted if you like, or you can create an empty one, just so the <link> can be resolved.


[BACK TO HOME](../README.md)