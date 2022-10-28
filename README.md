# java9-features-brief

1. Improved Javadoc
Java 9 update came with an updated Java documentation. 
We no longer need to use Google to find the right documentation. The new Javadoc came with search right in the API documentation itself. Moreover, the Javadoc output was HTML5 compliant. Every Javadoc page includes information on which JDK module the class or interface comes from.

2. Factory methods for collections(like List, Map, Set and Map.Entry):
Many a times, you want to create a collection (e.g., a List or Set) in your Java program and fill it with some elements. That leads to repetitive coding where you instantiate the collection, followed by several ‘add’ calls. With Java 9, several so-called collection factory methods have been added.
List and Set interfaces have “of()” methods to create an empty or no-empty Immutable List or Set objects as shown below:

```
Empty List example:
List immutableList = List.of();

Non-Empty List example:
List immutableList = List.of("one", "two", "three");
Map has two set of methods: of() methods and ofEntries() methods to create an Immutable Map object and an Immutable Map.Entry object respectively.

Empty Map Example:
jshell> Map emptyImmutableMap = Map.of()
emptyImmutableMap ==> {}

Non-Empty Map Example:
jshell> Map nonemptyImmutableMap = Map.of(1, "one", 2, "two", 3, "three")
nonemptyImmutableMap ==> {2=two, 3=three, 1=one}
```

4. Stream API Improvements:
In Java SE 9, Oracle Corp. has added four useful new methods to java.util.Stream interface. As Stream is an interface, all those new implemented methods are default methods. It allows you to create declarative pipelines of transformations on collections. There are four new methods added to the Stream interface: dropWhile, takeWhile, ofNullable. The iterate method gets a new overload, allowing you to provide a Predicate on when to stop iterating.

```
takeWhile()
dropWhile()
ofNUllable()
iterate()
```

5. Private methods in Interfaces:
In Java 8, we can provide method implementation in Interfaces using Default and Static methods. However we cannot create private methods in Interfaces. To avoid redundant code and more re-usability, Oracle Corp. introduced private methods in Java SE 9 Interfaces. From Java SE 9 on-wards, we can write private and private static methods too in an interface using ‘private’ keyword.
```
public interface Card{

  private Long createCardID(){
    // Method implementation goes here.
  }

  private static void displayCardDetails(){
    // Method implementation goes here.
  }

}
```

6. Multi-Resolution Image API:
In Java SE 9, Oracle Corp. introduced a new Multi-Resolution Image API. Important interface in this API is MultiResolutionImage . It is available in java.awt.image package. MultiResolutionImage encapsulates a set of images with different Height and Widths and allows us to query them with our requirements.

7. The Java(9) Platform module system:
One of the big changes or java 9 feature is the Module System. Oracle Corp. introduced the following features as part of Jigsaw Project:<br />
•	Modular JDK<br />
•	Modular Java Source Code<br />
•	Modular Run-time Images<br />
•	Encapsulate Java Internal APIs<br />
•	Java Platform Module System<br />

Before Java SE 9 versions, we are using Monolithic Jars to develop Java-Based applications. This architecture has lot of limitations and drawbacks. To avoid all these shortcomings, Java SE 9 comes with the Module System.

8. Improvements in Process API:
Java SE 9 is coming with some improvements in Process API. They have added couple new classes and methods to ease the controlling and managing of OS processes.<br />
Two new interface in Process API:<br />
•	java.lang.ProcessHandle<br />
•	java.lang.ProcessHandle.Info<br />

9. HTTP/2 Client
A new way of performing HTTP calls arrives with Java 9. As existing or Legacy HTTP Client API has numerous issues (like supports HTTP/1.1 protocol and does not support HTTP/2 protocol and WebSocket, works only in Blocking mode and lot of performance issues.), they are replacing this HttpURLConnection API with new HTTP client. They are going to introduce new HTTP 2 Client API under “java.net.http” package. It supports both HTTP/1.1 and HTTP/2 protocols. It supports both Synchronous (Blocking Mode) and Asynchronous Modes. It supports Asynchronous Mode using WebSocket API.
```
HttpClient client = HttpClient.newHttpClient();

HttpRequest req =
   HttpRequest.newBuilder(URI.create("http://www.google.com"))
              .header("User-Agent", "Java")
              .GET()
              .build();


HttpResponse resp = client.send(req, HttpResponse.BodyHandler.asString());
```

10. Miscellaneous Java 9 Features:<br />
•	GC (Garbage Collector) Improvements<br />
•	Stack-Walking API<br />
•	Filter Incoming Serialization Data<br />
•	Deprecate the Applet API<br />
•	Indify String Concatenation<br />
•	Enhanced Method Handles<br />
•	Java Platform Logging API and Service<br />
•	Compact Strings<br />
•	Parser API for Nashorn<br />
•	Javadoc Search<br />
