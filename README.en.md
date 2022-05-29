**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

<h1>
  Go <img src="./assets/go.svg" width="40" height="40" />
</h1>

<h2>Most Popular Go Interview Questions and Answers</h2>


<details>
<summary>1. What is Go and what tasks was it created for?</summary>

#### Go

Go (or Golang) is a compiled, statically typed programming language created at
Google by Robert Griesemer, Rob Pike, and Ken Thompson. It is designed with an
emphasis on simplicity, predictability, fast compilation and high performance in
production systems.

#### What Go was created for:

1. **Network and server systems:** HTTP/API services, proxies, gateways, backend
   for high-load applications.

2. **Cloud infrastructure:** orchestration tools, CI/CD, observability, DevOps
   utilities (which is why many cloud-native projects are written in Go).

3. **Concurrent computing:** tasks where parallel data processing, latency
   control and efficient use of resources are important.

4. **Application level system programming:** CLI tools, daemons, background
   workers, integration services.

#### Why Go:

- Concise syntax and low cognitive complexity of the code.

- Built-in concurrency model (`goroutine`, `channel`).

- Fast compilation and easy development cycle.

- Convenient standard toolkit (`go test`, `go vet`, `pprof`, modules).

Therefore, Go was created as a practical engineering language for scalable,
maintainable and high-performance services where reliability, development speed
and operational simplicity are important.

</details>


<details>
<summary>2. What are the main design principles of the Go language?</summary>

#### Go

Go's design is not based on maximum "expressiveness" at any cost, but on
engineering feasibility: the code must be easy to read, easy to maintain, and
reliable over the long life cycle of the system.

#### Basic principles of Go design:

1. **Simplicity over complexity:** The language deliberately avoids overly
   complex constructions to reduce the number of errors and the threshold of
   entry into the codebase.

2. **Readability and Unambiguity:** Clear code that can be quickly understood by
   any engineer on the team, not just the author, is preferred.

3. **Fast compilation and productive development:** The "wrote → built → tested"
   cycle should be short, which speeds up iterations in real projects.

4. **Built-in concurrency:** `goroutine` and `channel` are an organic part of
   the language, not an external patch, so parallel computing is natively
   supported.

5. **Composition over Heavy Hierarchy:** Go favors the approach of "composing
   behavior out of simple parts" rather than building deep inheritance chains.

6. **Minimalism in features, maximization in practicality:** less "magic", more
   predictable behavior during execution and debugging.

7. **Single tooling standard:** `go fmt`, `go test`, `go mod`, `go vet` form a
   common development culture without tooling fragmentation.

#### Generalization:

Go is designed as a language for team development and industrial programming: it
disciplines style, encourages clarity of thought in code, and provides a good
balance between simplicity and efficiency.

</details>
