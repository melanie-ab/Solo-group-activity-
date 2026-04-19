------------------------------
Group Member: Melanie Abarca
Answers to sakai questions are on: Group Activity 4: Concurrency file
------------------------------

[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=23619543)
## Group Activity on Concurrency using Scala Futures

In this group activity, we'll experiment with Scala futures. 

The `WebServiceClient` is a small wrapper for creating a number of concurrent web requests and observing progress from the client's perspective.   

For more details, see group activity 4 in Sakai.

```
❯ sbt console
...
scala> val c = new WebServiceClient
submitted request
defined direct results
defined other futures
ready for observation
val c: WebServiceClient = WebServiceClient@4d1ca627

scala> c.printProgress()
186
186

scala> c.printResults()
Some(Failure(java.net.ConnectException: handshake timed out after 10000ms))
None

scala> c.printProgress()
2293
2293

scala> all requests completed
108

scala> c.printResults()
Some(Failure(java.net.ConnectException: handshake timed out after 10000ms))
Some(Success(92))

scala> c.printProgress()
5001
5001
```
