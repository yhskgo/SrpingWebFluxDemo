# SpringWebFluxDemo

The WebFlux controller endpoint returns a Publisher in the form of either Flux or Mono. In the second method where we return all the students, it can be in the form of a Server-Sent Event (SSE) to the browser. For that, you need to define the return type as text/event-stream. The SSE is the technology allowing a browser to receive automatic updates from the server via an HTTP connection.

What does this mean? If we have a very huge stream, then the WebFlux controller will send the data as it receives from a reactive repository (from MongoDB in our case) and send it to the browser, instead of fetching all the records, which results in a blocking condition. This is how large volumes of streams are handled in Reactive Programming with Spring WebFlux.
