# NIO.2 socket tester

A demo application to check whether all successful writes can be read on the other end of the TCP socket using [AsynchronousByteChannel#write](http://docs.oracle.com/javase/7/docs/api/java/nio/channels/AsynchronousByteChannel.html#write%28java.nio.ByteBuffer,%20A,%20java.nio.channels.CompletionHandler%29).

### Building

The NetBeans *ant* project can be built in NetBeans just by running *ant* from command line:
```
ant
```

### Running

The jar file created in the dist folder contains both the server and client.

The server will listen on all available interfaces. To run it enter:
```
java -jar Nio2Test.jar
```

The client can be parameterized with a hostname (or IP address) if an interface other than "127.0.0.1" needs to be used to access the server:
```
java -cp Nio2Test.jar nio2test.Nio2TestClient [servername]
```
