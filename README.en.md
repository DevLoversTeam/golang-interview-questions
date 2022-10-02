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


<details>
<summary>3. What are the key features of Go compared to other languages?</summary>

#### Go

Go stands out because it combines concise syntax with a very practical
engineering model of execution: the language does not overload the developer
with unnecessary complexity, but provides tools for building fast and reliable
systems.

#### Key features of Go:

1. **Simple and strict syntax:** code is easy to read and stylistic uniformity
   is maintained automatically via `go fmt`.

2. **Compile to a native binary:** an application is usually compiled into a
   single executable without heavy external dependencies at startup.

3. **Static typing with high predictability:** a large number of errors are
   detected at the compilation stage, which increases reliability in production.

4. **Built-in concurrency:** `goroutine` and `channel` make parallel programming
   a natural rather than an auxiliary mechanism.

5. **Fast development cycle:** relatively fast compilation and standard tools
   accelerate testing and delivery of changes.

6. **Strong standard library:** networking, HTTP, cryptography, file
   manipulation, profiling, and testing available out of the box.

7. **Explicit error model:** In Go, errors are handled explicitly via `error`,
   making state control transparent and controllable.

8. **GC and Managed Memory:** The language simplifies system backend development
   without forcing you to manually manage the lifecycle of most objects.

9. **A practical modular approach:** `go mod` standardizes dependency management
   and build reproducibility.

#### Conclusion:

Unlike many languages that gravitate toward either maximum abstraction or
low-level controllability, Go purposefully maintains an engineering balance:
simplicity, performance, scalability, and team development convenience.

</details>


<details>
<summary>4. What is the difference between imperative and declarative programming paradigm? Give examples of languages.</summary>

#### Go

Imperative and declarative paradigms differ primarily in the focus of the
description: the first explains **how** to perform the task step by step, the
second — **what exactly** should be obtained as a result.

#### Imperative paradigm:

1. **Essence:** The programmer explicitly specifies the instruction sequence,
   state transitions, loops, branches, and execution order.

2. **Focus:** algorithm control and execution flow control.

3. **Typical traits:** variables, assignments, `for`, `if`, data mutation.

4. **Examples of languages:** Go, C, C++, Rust (in most practices), Java.

#### Declarative paradigm:

1. **Essence:** describes the desired result or properties of the system without
   detailing the implementation steps.

2. **Focus:** data model, rules and constraints, not algorithmic mechanics.

3. **Typical features:** higher-level expressions, minimization of explicit
   mutation, abstraction from execution order.

4. **Examples of languages/approaches:** SQL, HCL (Terraform), HTML/CSS,
   functional styles in Haskell and partly in Elixir.

#### Practical conclusion:

- In real systems, paradigms are often combined.

- Go is mostly imperative in nature, but some elements of declarativeness appear
  in configurations, schema descriptions, DSLs, and data queries.

- For the interview, it is important to emphasize that the choice of paradigm is
  not a question of "better or worse", but a question of matching the task, the
  team and the code support requirements.

</details>


<details>
<summary>5. Why is Go good for writing Cloud Native services?</summary>

#### Go

It is not by chance that Go is considered one of the most natural languages for
Cloud Native: its architectural properties match well with the requirements for
modern distributed systems — scalability, observability, reliability and
operational simplicity.

#### Why Go is effective in a Cloud Native environment:

1. **Lightweight concurrent computing:** `goroutine` and `channel` simplify the
   construction of services that handle large numbers of requests
   simultaneously.

2. **High performance and predictable runtime:** The Go compiler and optimized
   scheduler work well in busy network scenarios.

3. **Quick Start and Deploy:** typically the result of a build is a single
   binary that is easy to containerize and deploy to Kubernetes or other
   orchestrators.

4. **Low operational overhead:** Simple Docker images, fast build, less startup
   dependency issues.

5. **Powerful standard library:** `net/http`, `context`, `crypto`, `encoding`
   and other packages allow you to build production solutions without excessive
   dependence on third-party frameworks.

6. **Convenience of observability practitioners:** In Go, it is easy to
   integrate metrics, tracing and profiling, which is critical for cloud
   exploitation.

7. **Resistant ecosystem of infrastructure tools:** Much of the Cloud Native
   stack is written specifically in Go (e.g. Kubernetes, Prometheus, Helm,
   Terraform), which simplifies integrations and command context.

8. **Code clarity in team development:** Go encourages straightforward
   solutions, which reduces the cognitive load of supporting a microservice
   architecture.

#### Summary:

Go is well suited for Cloud Native services because it combines engineering
predictability with performance and practical convenience: from writing code to
its deployment, monitoring and long-term support.

</details>


<details>
<summary>6. What are `shadowing` variables and how can they cause errors in business logic?</summary>

#### Go

`Shadowing` (shadowing) is when a new variable is declared in the inner scope
with the same name as the outer one. As a result, the code does not work with
the "expected" variable, but with its local copy by name.

#### How it occurs most often:

1. **Short declaration `:=` in a nested block:** the developer expects an
   assignment, and in fact a new variable is created.

2. **Error handling (`err`) in `if`/`for`/`switch`:** local `err` overshadows
   the external one, causing subsequent state checks to fail.

3. **Working with state in long functions:** shading of intermediate variables
   makes reading more difficult and increases the risk of logical defects.

#### Why this is dangerous for business logic:

1. **False condition checks:** the system may jump to the wrong execution branch
   because the "wrong" variable is being checked.

2. **Lost or incorrect state:** for example, the calculation result remained in
   the local block and the external state was not updated.

3. **Complex debugging:** visually the name is the same, but semantically they
   are different objects; the error manifests itself inconspicuously and often
   only in combat cases.

4. **Quiet defects without panic:** a program may compile and run, but return a
   business-incorrect result.

#### How to prevent `shadowing`:

- Deliberately distinguish between `=` and `:=` in all nested blocks.

- Keep variable visibility short and avoid excessively long functions.

- Use clear, semantically accurate names, especially for states and errors.

- Connect static analysis (`go vet`, `golangci-lint`) with shading detection
  rules.

- In critical places of the logic, add tests for negative scenarios and boundary
  conditions.

#### Conclusion:

`Shadowing` is not a syntactic quirk, but a source of insidious logic errors. In
production Go code, the discipline of variable declaration directly affects the
correctness of the system's business behavior.

</details>


<details>
<summary>7. Why use `struct{}` (an empty struct) and in what scenarios is it effective?</summary>

#### Go

`struct{}` in Go is an empty struct, i.e. a fieldless type. Its key property: it
does not carry a data payload, but only records the very fact of the existence
of a value or event.

#### Why `struct{}` is effective:

1. **Null information volume:** type contains no fields, so it is used as a
   token, not a data container.

2. **Clear Intent Semantics:** the code explicitly shows that the "is/isn't"
   fact is important, not the payload.

3. **Reducing redundant allocations in service structures:** in many patterns
   this is a more practical choice than `bool` or arbitrary values ​​when data
   is not needed.

#### Typical usage scenarios:

1. **Set via `map[K]struct{}`:** `map` in Go is a key-value, and for a set we
   only need unique keys. `struct{}` here ideally means "key present".

2. **Signal channels `chan struct{}`:** are used for "event happened"
   notification (stop/done/shutdown) when no data needs to be transmitted.

3. **Token Types and API Contracts:** An empty structure can act as a
   lightweight semantic token in the application's internal protocols.

4. **Behavior Composition Embedding:** `struct{}` is sometimes used as a
   composition technical element when a stateless structure is required.

#### When not to use:

- When the actual state or attributes of an entity are required.

- When `bool` gives clearer business semantics (eg an explicit condition flag
  rather than a set fact).

#### Summary:

`struct{}` is a tool for precise intent: if data is not needed, but a fact,
presence, or signal needs to be indicated, an empty structure is an elegant and
efficient solution in Go code.

</details>


<details>
<summary>8. How does the `slice` internal structure work and what happens when you pass it to a function?</summary>

#### Go

In Go, `slice` is not the array itself, but a lightweight “add-on” descriptor
over a section of the array. This is why the behavior of `slice` differs from
normal array copying and often causes errors in interviews and real code.

#### Internal model `slice`:

`slice` conceptually consists of three parts:

1. **Pointer to base array** (`ptr`)

2. **Length** (`len`) - how many items are available now

3. **Capacity** (`cap`) — how many elements are available up to the limit of the
   base array

That is, `slice` stores metadata about the region in memory, rather than
duplicating all elements.

#### What happens when you pass `slice` to a function:

1. **The `slice` header (ptr/len/cap) is copied, not the entire array.**

2. **Both parties (caller and callee) initially look at the same base array.**

3. **Changing elements via index** (`s[i] = ...`) in the function is usually
   visible from the outside, because the data of the shared array is changed.

4. **Changing the header itself** (`s = s[:n]`, `s = append(...)`) in a function
   does not change the header in the caller unless you return a new `slice`.

#### Key nuance with `append`:

- If there is enough `cap` during `append`, the entry goes to the same base
  array.

- If `cap` is missing, the runtime allocates a new array, copies the data there,
  and the local `slice` in the function starts referring to another memory.

So, after `append` the function can already work with the new array, while the
old `slice` will remain outside if the new value is not returned.

#### Practical conclusion:

- Want to change elements - you can pass `slice` as is.

- Want to change the length/capacity or result of `append` - return the updated
  `slice` from the function (or pass a pointer to `slice` when truly
  architecturally justified).

#### Example:

```go
package main

import "fmt"

func grow(s []int) {
	s = append(s, 99) // змінюємо локальний заголовок slice
}

func mutate(s []int) {
	s[0] = 42 // змінюємо спільний базовий масив
}

func main() {
	s := []int{1, 2, 3}
	mutate(s)
	grow(s)
	fmt.Println(s) // [42 2 3], append у grow не змінив заголовок у викликачі
}
```

</details>


<details>
<summary>9. Why is `make([]T, 0, n)` better than `var s []T` given the known dimensions?</summary>

#### Go

When you know the approximate or exact number of elements in advance, the
`make([]T, 0, n)` construct is almost always more practical than `var s []T`
because it immediately reserves the required capacity and reduces the number of
memory reallocations.

#### What distinguishes these two approaches:

1. **`var s []T`**

- creates `nil`-slice from `len=0`, `cap=0`;

- the first `append` causes the runtime to allocate memory;

- as data grows, new reallocations and copies occur.

2. **`make([]T, 0, n)`**

- creates a slice from `len=0`, but already from `cap=n`;

- elements are added via `append` without reallocation until `cap` is exhausted;

- fewer data copies and more stable performance.

#### Why it is important in practice:

1. **Less allocations in the heap:** reduces GC load.

2. **Better latency-behavior:** less "jumps" in reallocation time.

3. **Higher throughput in hot paths:** especially in loops, parsing,
   aggregation, serialization.

4. **Resource predictability:** easier to estimate memory for a specific
   scenario.

#### When the difference is particularly noticeable:

- Large number of `append` in loops.

- Processing of data streams in backend services.

- Frequently called functions where even small allocations accumulate into
  significant costs.

#### Conclusion:

If the size of the collection is known or well estimated in advance, `make([]T,
0, n)` is an engineering-mature choice: it gives fewer allocations, better
performance, and more stable behavior under load.

</details>


<details>
<summary>10. How does a slice expression `a[low:high:max]` control `cap` a new slice?</summary>

#### Go

In Go, the full slice form `a[low:high:max]` allows you to control not only the
length (`len`) but also the capacity (`cap`) of the new `slice`. This is an
important tool for controlling side effects during `append`.

#### Formulas:

For `s := a[low:high:max]`:

1. `len(s) = high - low`

2. `cap(s) = max - low`

Under the condition of correct limits:

- `0 <= low <= high <= max <= cap(a)` (for slice base)

#### What it gives practically:

1. **Visible capacity limitation:** you can "cut off" access to the tail of the
   underlying array even if it physically exists.

2. **Safer `append`:** if `cap` is artificially reduced, `append` will
   reallocate memory faster instead of overwriting adjacent data in the shared
   array.

3. **Better isolation between pieces of code:** this is especially useful when
   one slice is passed to another function or system layer and you don't want it
   to "grow" into someone else's area.

#### Conceptual example:

- `a[2:5]` gives `len=3`, `cap` extends to the end of the base array.

- `a[2:5:5]` gives `len=3`, `cap=3` - further `append` is out of stock and
  forces a new array.

#### Conclusion:

The third index in `a[low:high:max]` is the precision control lever `cap`. It is
needed when it is important to control the growth of `slice`, avoid unexpected
overwriting of shared memory, and make code behavior predictable.

#### Example:

```go
package main

import "fmt"

func main() {
	a := []int{0, 1, 2, 3, 4, 5}
	s := a[2:4:4] // len=2 (2,3), cap=2
	fmt.Println(len(s), cap(s)) // 2 2

	s = append(s, 99) // новий backing array, а не розширення в a
	fmt.Println(a)    // [0 1 2 3 4 5]
	fmt.Println(s)    // [2 3 99]
}
```

</details>


<details>
<summary>11. Is a pointer to a slice element guaranteed to remain valid after calling `append`?</summary>

#### Go

Short answer: **no, not guaranteed**. After `append`, a pointer to an element of
the old `slice` may lose its relevance to the new `slice` if the underlying
array has been reallocated.

#### Why this happens:

1. `append` adds elements within the existing `cap` if there is enough space.

2. If `cap` is exhausted, the runtime creates a new array, copies the data, and
   returns `slice`, which already refers to the new address.

3. Previously taken pointers remain bound to the old array, not the updated
   `slice`.

#### Practical consequences:

1. **Pointer aliasing becomes dangerous:** logic can "look" into an outdated
   memory area.

2. **Unexpected bugs in modifications:** changes through the old pointer do not
   affect the new `slice` after relocation.

3. **Difficult Debugging:** code compiles and often runs, but exhibits
   unpredictable behavior under load or on other data volumes.

#### How to write safely:

- Do not store long-lived pointers to `slice` elements that will potentially
  grow through `append`.

- If the pointer is really needed, ensure memory stability: pre-reserve capacity
  (`make(..., 0, n)`) or do not execute `append` after taking addresses.

- It is often safer to pass an index or return a new `slice` and bind all
  derived references.

#### Conclusion:

After `append`, the validity of pointers to `slice` elements is not a Go
contract. Secure code must assume that `append` can change the base address of
the data.

</details>


<details>
<summary>12. How to efficiently remove elements from a slice without preserving order in Go?</summary>

#### Go

If the order of the elements does not matter, the most efficient removal
strategy is to replace the element being removed with the last element of
`slice` and then shorten `slice` by one.

#### The idea of the approach:

1. Find the index `i` of the element to delete.

2. Assign `s[i] = s[len(s)-1]`.

3. Reduce length: `s = s[:len(s)-1]`.

#### Why it is effective:

1. **O(1) in time** (without shifting all subsequent elements).

2. **Minimum copies** compared to in-order deletion.

3. **Scales well** on large collections and hot loops.

#### What to pay attention to:

- The order of elements changes after the operation.

- Checking the correctness of the index is required.

- For `slice` with pointer types, it is sometimes appropriate to null the tail
  element before truncation to avoid keeping redundant references in memory.

#### Conclusion:

When stable order is not a business logic requirement, "swap with last +
truncate" is the canonical and fastest way to remove an element from `slice` in
Go.

#### Example:

```go
func removeUnordered[T any](s []T, i int) []T {
	last := len(s) - 1
	s[i] = s[last]
	var zero T
	s[last] = zero // опційно: щоб не тримати зайве посилання
	return s[:last]
}
```

</details>


<details>
<summary>13. What is the key iteration order in `map` and can it be relied upon? How does this affect tests and serialization?</summary>

#### Go

In Go, the iteration order of the keys in `map` is **non-deterministic**. This
means that during `for range` the key sequence can vary between program runs and
even between individual iterations within a single run.

#### Can you rely on the order:

1. **No, you can't.**

2. The order in `map` is not part of the language contract.

3. Any logic that implicitly relies on a "stable" order is potentially flawed.

#### How it affects the tests:

1. **Flaky tests:** comparisons of strings/arrays formed with `map` may randomly
   fail due to different order of elements.

2. **False regressions:** there are no changes in the business logic, but the
   test fails due to unstable output.

3. **Correct approach:** tests require either:

- compare structures as sets/associative collections;

- or presort the keys and build a deterministic result.

#### How this affects serialization:

1. If the serialization is built on a direct `map` bypass, the text result may
   have a different order of fields/key-value pairs.

2. This makes it difficult:

- snapshot/golden-tests;

- hashing of payloads;

- artifact comparison in CI.

3. For a stable output, you should:

- get keys separately;

- sort them;

- form the result in a fixed sequence.

#### Conclusion:

`map` in Go is optimized for fast access by key, not order-preserving.
Therefore, tests, logging, data signing, and serialization need to deliberately
introduce determinism through key sorting or other canonical rules.

</details>


<details>
<summary>14. How to iterate over `map` in a predictable order?</summary>

#### Go

Since `map` in Go does not guarantee a stable traversal order, the intended
iteration must be organized explicitly: first collect the keys, then sort them,
and only then read the values in this fixed order.

#### Canonical approach (Go 1.23+):

1. Use `maps.Keys` to get a key iterator.

2. Use `slices.Sorted` (`slices.SortedFunc`) to get a sorted key slice.

3. Iterate over the sorted slice.

#### Why it's right:

1. **Determinism:** the same input gives the same order of output.

2. **Stable tests:** random crashes due to different sequence disappear.

3. **Predicted serialization:** easier to do golden tests, signatures, compare
   artifacts.

#### Important nuances:

- An explicit sort criterion must be defined for structure keys or custom types.

- Difficulty increases due to sorting (`O(n log n)`), but that's the price of
  predictability.

- If order is critical in a hotpath, it is sometimes appropriate to consider a
  different data structure (eg maintaining a separate ordered list of keys).

#### Conclusion:

The intended iteration of `map` in Go is always a conscious three-phase
strategy: "collect keys → sort → traverse". This pattern is considered the
production standard for stable output. A compact form via
`slices.Sorted(maps.Keys(m))` is available since Go 1.23.

#### Example:

```go
keys := slices.Sorted(maps.Keys(m))
for _, k := range keys {
	fmt.Printf("%v=%v\n", k, m[k])
}
```

</details>


<details>
<summary>15. Why can't I get the address of the map element?</summary>

#### Go

In Go, you cannot take the address of the `map` element (for example,
`&m[key]`), because the value in `map` does not have a stable address in memory.
During growth, rebalancing, or internal reorganization, the `map` runtime may
move items between buckets.

#### Key reason for limitation:

1. **Placement Instability:** `map` changes the internal structure dynamically.

2. **Danger of "dangling" pointers:** the address obtained today may become
   invalid after subsequent operations with `map`.

3. **Guarantee of language safety:** the compiler prohibits this operation to
   avoid hidden memory bugs.

#### Practical consequences:

1. You cannot modify a structure field directly via `m[key].Field = ...` if the
   map value is a structure.

2. The update pattern for map-value-struct looks like this:

- read value into temporary variable;

- change it;

- write back to `map`.

#### When mutability is needed at:

- Use `map[K]*T` instead of `map[K]T` if you need to work with the same object
  via pointer.

- But be aware of the trade-offs: additional allocations, object lifecycle
  issues, and the need for synchronization with concurrent access.

#### Conclusion:

The prohibition against taking the address of the `map` element is a deliberate
Go design in favor of memory-safety. If "in-place" changes are required, choose
either a read-modify-write loop or `map` with pointer values.

</details>


<details>
<summary>16. Why is `map` not thread-safe out of the box in Go?</summary>

#### Go

`map` in Go is not thread-safe by design: simultaneous access from multiple
goroutines without synchronization (especially when there is a record) leads to
data races and undefined behavior.

#### Why is this done:

1. **Performance in base scenario:** most `map` are used locally in a single
   goroutine; a built-in lock for each operation would make these scenarios
   slower.

2. **Explicit model of competition:** Go puts control of synchronization on the
   developer, so that he chooses a mechanism for a specific workload.

3. **Architecture flexibility:** different tasks require different strategies
   (mutex, sharding, actor-approach, `sync.Map`), and a "one-size-fits-all"
   autolock is not optimal for all cases.

#### What this means in practice:

1. **Concurrent read + write without protection is prohibited.**

2. **Write + write without protection is prohibited.**

3. **Read + read only** can be safe if no one modifies `map`.

#### How to do it right:

- `map` + `sync.Mutex` or `sync.RWMutex` for managed synchronization.

- `sync.Map` for specific access patterns (many reads, rare writes, or
  independent keys).

- Architectural state isolation through one "proprietary" goroutine and
  channels.

#### Conclusion:

`map` non-flow safety out of the box is not a flaw, but a conscious compromise
of Go: minimal overhead in the general case and full control of concurrency in
the hands of the engineer.

</details>


<details>
<summary>17. Can a struct be a key in `map` and what are the restrictions on that? How is it better than nested maps?</summary>

#### Go

Yes, in Go a structure can be a key in `map` **if it is compared**
(`comparable`). This means that all its fields must also be comparable.

#### Restrictions for the struct key:

1. **All fields of the structure must be comparable.**

- Permitted, in particular: numbers, strings, bool, pointers, arrays (with
  comparable elements), other comparable structures.

- Prohibited fields of types in the key: `slice`, `map`, `func` (they are not
  comparable).

2. **The comparison is based on the value of all fields.**

- Two keys are considered equal only if all corresponding fields are equal.

3. **Key must be stable after insertion.**

- Changing the "sense" of a key through external mutable state is a bad practice
  because it destroys the predictability of access.

#### Why struct-key is often better than nested `map`:

1. **A simpler data model:**

- Instead of `map[A]map[B]V`, you can use `map[CompositeKey]V`, where
  `CompositeKey` is a structure with fields `A`, `B`.

2. **Less boilerplate and checks on `nil`:**

- In nested `map` internal maps must be initialized and intermediate missing
  keys handled.

3. **Better logic locality:**

- All key dimensions are collected in one type, which improves readability and
  maintainability.

4. **Less room for error:**

- Easier to avoid partially initialized structures and inconsistent access
  paths.

#### When nested `map` may be appropriate:

- When hierarchical data semantics are required.

- When frequently operating with intermediate slices at the level of the first
  key.

- When different tiers have separate lifecycle rules.

#### Conclusion:

Go's struct key is a powerful and clean tool for composite addressing. If the
key type is correctly designed and is `comparable`, this solution is often more
elegant and reliable than nested `map`.

</details>


<details>
<summary>18. How to compare two structures - when it compiles and when it doesn't?</summary>

#### Go

In Go, two structures can be compared with the `==` or `!=` operator only when
the type of the structure is `comparable`. Practically, this means: **all fields
of the structure must be compared**.

#### When the comparison is compiled:

1. The structures have the same type.

2. Each field in the structure is comparable-type.

3. Comparison is performed on the value of all fields.

#### When the comparison does not compile:

1. If at least one field has a noncomparable type:

- `slice`

- `map`

- `func`

2. If trying to compare different structure types, even with similar fields.

#### Important clarifications:

1. **Arrays are compared** if their elements are compared.

2. **Pointers are compared** (addresses are compared).

3. **Interfaces are compared** if the dynamic value inside is also compared;
   otherwise runtime panic during comparison is possible.

#### Practical conclusion:

- If the structure is entirely of comparable-fields, feel free to use `==`.

- If the structure is `slice/map/func`, use explicit field comparison or
  separate approaches (such as specialized comparison logic) rather than a
  direct equality operator.

</details>


<details>
<summary>19. How to implement a comparison of two structures if they contain slices or maps? What is `reflect.DeepEqual()`?</summary>

#### Go

If the structure contains `slice` or `map`, a direct comparison via `==` does
not compile. In such cases, the comparison should be implemented separately:
either manually or with the help of deep comparison utilities.

#### Basic approaches:

1. **Explicit field comparison (recommended for critical logic):**

- compare simple fields directly;

- for `slice` check length and elements;

- for `map` check the number of keys and matching values.

2. **`reflect.DeepEqual(a, b)`:**

- performs recursive ("deep") comparison of complex structures;

- handy for quick checks, prototypes and part of test scenarios.

#### What is `reflect.DeepEqual()`:

`reflect.DeepEqual()` is a function of the standard package `reflect` that
attempts to determine the deep equality of two values by traversing nested
fields, collection elements, and data structures recursively.

#### Nuances `reflect.DeepEqual` that are important to remember:

1. **Semantics may not match business equality:**

- for example, `nil`-slice and empty `[]T{}` are often treated differently.

2. **Less transparent diagnostics:**

- when falling, it is more difficult to understand which field is different
  without additional tools.

3. **Performance:**

- reflection is slower than specialized manual comparison in hotpaths.

#### When to choose:

1. **Production-business-rules:** explicit domain comparison (clear semantics).

2. **Tests and auxiliary checks:** `reflect.DeepEqual` or more specialized test
   libraries.

3. **Critical scenarios:** avoid reflection "magic" where strict equivalence
   checking is required.

#### Conclusion:

For structures with `slice/map`, the correct comparison is primarily a matter of
semantics, not technique. `reflect.DeepEqual()` is a useful tool, but an
explicit, domain-based comparison method remains the most reliable engineering
method.

</details>


<details>
<summary>20. What happens when casting between named types with the same structure if they have different methods?</summary>

#### Go

In Go, casting between named types with the same child structure applies **only
to data values**, but does not "port" methods. That is, after conversion, you
get a new value of another named type with its own method set.

#### The main principle:

1. **The conversion changes the type of the value rather than unifying the
   behavior of the types.**

2. **Methods belong to the specific named type** on which they are declared.

3. After `T2(vT1)`, the `T2` methods are available, and the `T1` methods are no
   longer directly accessible.

#### What is saved during conversion:

1. Bit/Boolean representation of fields (according to type compatibility rules).

2. Data value.

#### What is not saved:

1. Method-set of the original type.

2. Automatic interface matching provided by the original type.

#### Practical consequences:

1. Two types with the same fields can have different behavior in the API.

2. After conversion, code may fail to compile in places where an interface
   implemented only by the source type was expected.

3. This is useful for domain modeling: same data structure but different
   semantic roles and contracts.

#### Conclusion:

In Go, converting between named types is changing the "identity" of the type,
not copying behavior. The data may be the same, but the methods and interface
capabilities are defined solely by the target type.

</details>


<details>
<summary>21. What is `Memory Alignment` (alignment) and how does it affect the size of structures?</summary>

#### Go

`Memory Alignment` (alignment) is a rule for placing data in memory at addresses
multiples of a certain step (alignment requirement) for a specific type. The
processor and runtime read such data faster and more safely when these
requirements are met.

#### How it works in frameworks:

1. Each field has its own alignment requirement (eg `int64` usually requires
   stricter alignment than `byte`).

2. Between the fields, the compiler can add **padding** (placeholder service
   bytes) so that the next field starts at the correct address.

3. There can also be tail-padding at the end of a structure so that an array of
   such structures preserves the correct alignment of each element.

#### Impact on structure size:

1. **The structure size is often larger than the sum of the field sizes** due to
   padding.

2. **Field order matters:** bad placement (`byte`, `int64`, `byte`, ...) can
   significantly increase the total size.

3. **Optimal grouping of fields** (from larger aligned to smaller) usually
   reduces memory usage.

#### Why it is important in practice:

1. Smaller structure size = better cache locality.

2. Less RAM consumption in large arrays/caches/indexes.

3. Higher throughput in hot paths due to reduced memory pressure.

#### Engineering conclusion:

Alignment is not a "low-level exotic", but a practical performance factor. In
Go, the correct order of fields in a structure directly affects its size, and
therefore memory efficiency and system speed.

</details>


<details>
<summary>22. Why is passing a large structure "by value" often slower than passing a pointer?</summary>

#### Go

Passing a large structure by value means copying its entire contents each time
the function is called. For bulk types, this can be significantly more expensive
than passing a single pointer to the same data.

#### Why there is a difference in performance:

1. **Memory copy cost:** the larger the structure, the more bytes need to be
   copied on I/O calls.

2. **Load on processor cache:** massive copies increase memory traffic and can
   degrade cache locality in hot code areas.

3. **Cascading effect in loops and pipelines:** if a structure is passed
   multiple times, overhead accumulates.

4. **Potential Impact on Allocations:** In some scenarios, copy and escape
   behavior can increase runtime and GC pressure.

#### When a pointer is often better:

1. When the structure is large and often passed between functions.

2. When you need to change the shared state without additional copying.

3. When stable latency behavior under load is important.

#### But not always a pointer is automatically better:

1. For small structures, passing by value can be simpler and quite efficient.

2. Value gives better state isolation (no implicit shared mutable state).

3. Pointer adds aliasing risks and the need for more careful synchronization in
   competing code.

#### Practical conclusion:

In Go, the choice between value and pointer is not made dogmatically, but based
on the data profile: large structures and frequent calls favor the pointer;
small immutable-like data is often appropriate to pass by value.

</details>


<details>
<summary>23. Why is `map` slower than `slice` with sequential access and when to choose what?</summary>

#### Go

For sequential access (`sequential access`), `slice` is usually faster than
`map` because the elements of `slice` are compact and read linearly, while `map`
performs key hashing and access to a more complex internal structure.

#### Why `slice` is faster in a sequential pass:

1. **Linear placement in memory:** elements are next to each other, which
   matches well with CPU caches.

2. **Simple access by index:** minimum auxiliary operations per element.

3. **Better predictability for the processor:** linear pattern reduces the
   number of cache misses.

#### Why `map` is slower in this scenario:

1. **Hashing keys** adds computational overhead.

2. **Uneven bucket placement** is worse for memory locality.

3. **More complex access logic** (search in buckets, collisions, service
   checks).

#### When to choose `slice`:

1. Data is passed sequentially.

2. Requires iterations, sorting, batch processing.

3. The key is actually a position (index), not an arbitrary identifier.

#### When to choose `map`:

1. Requires fast key access (`id`, `name`, composite key).

2. Set/dictionary semantics are important.

3. Search by key value dominates full linear traversal.

#### Practical conclusion:

`slice` — a tool for orderly, dense iterations; `map` — for address access by
key. If the workload is mostly sequential, `slice` usually gives better
performance and lower overhead.

</details>


<details>
<summary>24. How to check if a variable implements an interface?</summary>

#### Go

In Go, the implementation of an interface is implicit: a type is considered to
implement an interface if it has the entire required set of methods. Therefore,
verification is possible both at the compilation stage and at runtime.

#### 1) Verification at the compilation stage (recommended):

The most reliable approach is to add a compile-time assertion:

```go
var _ MyInterface = (*MyType)(nil)
```

What this means:

1. If `*MyType` does not implement `MyInterface`, the code will not compile.

2. This documents the type contract directly in the codebase.

3. Especially useful for public APIs, adapters, and large commands.

#### 2) Check during execution (runtime):

When there is a value of type `any`/interface, type assertion is used:

```go
v, ok := x.(MyInterface)
```

1. `ok == true` — the value implements the interface.

2. `ok == false` — does not implement.

3. Variant without `ok` can cause panic, so production code usually uses the
   safe form with `ok`.

#### Pointer vs value receiver — a critical nuance:

1. The `T` and `*T` method sets are different.

2. Often it is `*T` that implements the interface and `T` does not.

3. In the interview, it is important to talk about this point clearly, because
   it is a typical source of mistakes.

#### Conclusion:

The best practice is to fix the implementation of the interface with a
compile-time assertion, and to use runtime verification via assertion where the
type of the value is known only at runtime.

</details>


<details>
<summary>25. What are `type assertion` and `type switch` - what are their benefits and how to handle assertion without panic?</summary>

#### Go

`type assertion` and `type switch` in Go are mechanisms for working with
interface values when the actual (dynamic) type needs to be specified at
runtime.

#### What is `type assertion`:

`type assertion` has the form:

```go
v, ok := x.(T)
```

1. `x` — interface type value.

2. `T` is the type we are trying to lead to.

3. `ok == true` means that the dynamic type is compatible with `T`.

#### Benefit `type assertion`:

1. Allows access to specific behavior of a specific type.

2. Enables safe work with `any`/interfaces in adapters, decoders, middleware.

3. Useful when one specific type is expected.

#### How to avoid panic:

Dangerous form:

```go
v := x.(T) // panic, якщо x не є T
```

Safe form:

```go
v, ok := x.(T)
if !ok {
    // обробити невідповідність типу
}
```

It is the two-digit form with `ok` that is the production standard.

#### What is `type switch`:

`type switch` is a convenient way to handle several possible types at once:

```go
switch v := x.(type) {
case string:
    // ...
case int:
    // ...
default:
    // ...
}
```

#### Benefit `type switch`:

1. Makes type branching readable.

2. Reduces the cascade of multiple assertions.

3. Gives an explicit `default` path for unknown types.

#### When to use what:

1. **`type assertion`** — when checking one expected type.

2. **`type switch`** — when we allow several types and need different logic for
   each.

#### Conclusion:

`type assertion` and `type switch` are a controlled way to "expose" a dynamic
interface value type. To avoid crashes, assertion should be made in safe form
`v, ok := ...` and always have a processing script `ok == false`.

</details>


<details>
<summary>26. Why are `interface{}` and `any` identical, but `*interface{}` is almost always a mistake?</summary>

#### Go

In Go, `any` is just an alias (`alias`) for `interface{}`. That is, from the
point of view of a typical system, they are absolutely the same: the difference
is only stylistic and semantic for code readability.

#### Why `interface{}` == `any`:

1. `any` is introduced for better clarity, especially in generics code.

2. The compiler interprets `any` and `interface{}` as the same type.

3. The behavior during assignment, assertion, switch is identical.

#### Why `*interface{}` is almost always an error:

1. **An interface is already a "reference container" for value + type.** Adding
   another pointer level usually doesn't make sense.

2. **Complication of nil semantics:** with `*interface{}` another layer of
   states appears (`nil` pointer, non-zero pointer on nil-interface, etc.),
   which generates non-obvious bugs.

3. **Poor readability and API design:** this type almost always signals that the
   data model or function signature is poorly designed.

4. **Instead of `*interface{}` usually suffices:**

- or pass `interface{}`/`any` by value;

- or use a specific pointer type (`*T`) if the mutability of the `T` object is
  required.

#### When `*interface{}` can happen:

- In narrow technical scenarios (where exactly an interface variable like a cell
  needs to be changed), but in applied production code, this is a rare and
  mostly undesirable pattern.

#### Conclusion:

`any` and `interface{}` are identical. Instead, `*interface{}` is in most cases
an unnecessary abstraction that complicates the code and increases the risk of
logic errors.

</details>


<details>
<summary>27. When should `interface{}` (`any`) be used, and when is it considered bad tone?</summary>

#### Go

`any` (ie `interface{}`) is appropriate where the type of the value is
objectively unknown at the API boundary. However, excessive use of `any` in
domain logic usually degrades type safety and makes maintenance difficult.

#### When `any` is truly justified:

1. **Infrastructure layers and universal containers:** logging, generic
   wrappers, middleware, low-level libraries.

2. **Decoding weakly typed formats:** such as JSON parts with unpredictable
   schema.

3. **Integration points with external APIs:** when the contract is dynamic and
   the strict type cannot be fixed in advance.

4. **Transitional refactoring steps:** as a temporary compromise with a
   subsequent return to concrete types.

#### When it's a bad tone:

1. **In a business model where the type is known:** `any` hides errors until
   runtime instead of compile-time.

2. **When `any` replaces normal API design:** multiple assertions and type
   switches in every other place are a symptom of undefined contracts.

3. **When you can use generics or an interface with a minimal method:** this
   gives stricter and more readable constraints.

4. **When `any` gets "all over the place" by inertia:** code becomes fragile,
   harder to test, and harder to evolve.

#### Rule of thumb:

- Default choose **specific type**.

- If behavior abstraction is required — **interface with clear contract**.

- If data generalization is required — **generics**.

- `any` leave for truly dynamic system boundaries.

#### Conclusion:

`any` is a useful tool, but not a one-size-fits-all answer. In mature Go code,
it is used point-wise: where type ambiguity is natural, and not where a strict
contract can and should be expressed.

</details>


<details>
<summary>28. What is the advantage of accepting interfaces and returning specific structures?</summary>

#### Go

In Go, there is a common and extremely practical principle: **accept interfaces,
return structures**. Its strength lies in keeping input dependencies flexible
and output contracts clear and feature-rich.

#### What does "accept interfaces" mean:

1. The function/method accepts a minimal behavior contract (eg `io.Reader`)
   rather than a hard-coded type.

2. This reduces coupling between modules.

3. Simplifies testing: easy to substitute stub/mock/fake with required methods.

#### What does "return structures" mean:

1. The call receives a concrete type with its full set of methods.

2. API becomes more transparent: the user sees the real capabilities of the
   object.

3. Easier to evolve a type without breaking external interface contracts.

#### Why this combination is effective:

1. **At the entrance — abstraction, at the exit — concreteness.**

2. **Higher integration flexibility** without losing API expressiveness.

3. **Better maintainability:** module boundaries are clear, dependencies are
   controlled.

4. **Easier Refactoring:** Internal changes are easier to make without cascading
   edits.

#### When to be careful:

1. Do not create fallback interfaces without real need.

2. An interface should live where it is consumed, not where it is implemented.

3. If only one implementation is needed and there is no test benefit, too much
   abstraction can hurt readability.

#### Conclusion:

Accepting interfaces and returning concrete structures is a balance between
extensibility and clarity. It allows you to write Go code that is at the same
time convenient to test, easy to maintain and naturally develop.

</details>


<details>
<summary>29. Why does Go use single-method interfaces (eg `io.Reader`, `fmt.Stringer`) and what architectural benefit does it provide?</summary>

#### Go

Single-method interfaces in Go are a concentrated behavior contract: they
describe exactly one ability of an object, without overloading the API. That is
why `io.Reader`, `io.Writer`, `fmt.Stringer` became the fundamental building
blocks of the ecosystem.

#### Why this approach is so powerful:

1. **Minimum contract:** type only needs to implement one method to integrate
   with a large number of components.

2. **Low Coupling:** Modules depend on a capability, not a specific
   implementation or a big "fat" interface.

3. **Compositibility:** complex capabilities are easily built from combinations
   of small interfaces.

4. **Simple testing:** a small fake/stub with one method is enough for the test.

#### Architectural benefit:

1. **Plugin-like interchangeability of implementations:** file, network socket,
   in-memory buffer can work equally as `io.Reader`.

2. **Stable module boundaries:** dependencies between system layers become clear
   and evolutionarily stable.

3. **Easy code evolution:** new implementation can be added without changing
   consumers if the contract is preserved.

4. **Readability of intent:** the function signature immediately answers the
   question "what is required of the argument".

#### Practical conclusion:

Single-method interfaces are not a stylistic decoration, but an architectural
strategy of Go: small contracts, high composability, easy testability, and
controlled scalability of the system.

</details>


<details>
<summary>30. Why is `nil != nil` in Go and how does it relate to interfaces?</summary>

#### Go

The phrase "`nil != nil`" in Go usually refers to interfaces and means that an
interface value can contain **type + value** where the value inside is `nil`,
but the interface itself is not `nil`.

#### How the interface is arranged conceptually:

The interface consists of two parts:

1. **Dynamic Type**

2. **Dynamic Value**

An interface is `nil` only when **both** parts are missing.

#### Where the trap occurs:

1. We have `var p *MyType = nil`.

2. Assign `var i any = p`.

3. Now `i` contains:

- type: `*MyType`

- value: `nil`

So `i != nil` because the typical part is filled.

#### Practical consequences:

1. The `if err != nil` or `if x != nil` check may not behave as the developer
   expects if typed nil is wrapped in the interface.

2. This is a typical source of bugs in errors, factories, middleware, DI code.

#### How to avoid problems:

1. Return `nil` exactly as "empty interface", not typed nil inside the
   interface.

2. Construct `error` and other interface results with care.

3. When necessary, do explicit checking of a specific type via assertion/switch.

#### Conclusion:

In Go, "`nil != nil`" is not a paradox, but a consequence of the two-component
nature of the interface. The key rule is that an interface is `nil` only when it
contains neither a dynamic type nor a dynamic value.

#### Example:

```go
var p *bytes.Buffer = nil
var x any = p

fmt.Println(p == nil) // true
fmt.Println(x == nil) // false: type=*bytes.Buffer, value=nil
```

</details>


<details>
<summary>31. Can methods be called on `nil` values and where is this actively used?</summary>

#### Go

Yes, in Go, a method can be called on a `nil` value, **if this is permissible
from the point of view of the receiver type**. Most often, we are talking about
methods with a pointer receiver (`*T`), where the receiver can be `nil`.

#### Key idea:

1. Calling a method on a `nil`-pointer is technically possible.

2. The question is what the method code does inside.

3. If the method denames receiver without checking, we will get panic.

#### When it works safely:

1. The Method explicitly handles the `nil` receiver:

- returns the default value;

- returns error;

- behaves as a no-op.

2. This design is sometimes deliberately used for a convenient API.

#### Where this is actually used:

1. **Error types and wrappers:** methods on pointer types can work correctly
   with `nil` to simplify error handling.

2. **Linked/list/tree-like structures:** `nil`-node can be interpreted as an
   empty state with correct behavior.

3. **Service objects with optional components:** `nil` receiver is sometimes
   used as "disabled" or "empty" mode.

#### An important nuance with interfaces:

If a `nil` pointer is wrapped in an interface, the interface itself may not be
`nil`. Therefore, checks for `nil` should be done carefully to avoid false
confidence.

#### Practical conclusion:

Methods on `nil` values in Go are a legitimate tool, but only with conscious API
design: either safe handling of `nil` inside the method, or clear documentation
that a call to `nil` is not allowed.

</details>


<details>
<summary>32. How to tell the main goroutine to wait for all worker goroutines to finish?</summary>

#### Go

The canonical way to wait for all working goroutines to complete in Go is to use
`sync.WaitGroup`. It provides a simple and robust pattern: increment the counter
before starting the job, decrement it after it's done, and call `Wait()` in the
main goroutine.

#### Basic scheme:

1. Create `var wg sync.WaitGroup`.

2. Before each goroutine call `wg.Add(1)`.

3. Inside the goroutine execute `defer wg.Done()`.

4. In the main goroutine call `wg.Wait()`.

#### Why it works:

1. `WaitGroup` counts the number of unfinished tasks.

2. `Wait()` blocks execution until the counter reaches zero.

3. This ensures that `main` will not terminate before the working goroutines.

#### Typical mistakes to avoid:

1. Call `Add(1)` **after** the start of the goroutine (risk of race and
   incorrect termination).

2. Forget `Done()` in the bug or early `return` branch.

3. Reusing the same `WaitGroup` in different phases without clear
   synchronization.

#### When is better `errgroup`:

If, in addition to waiting, you also need:

1. collect the first error,

2. cancel other tasks via `context`,

then it is more practical to use `errgroup.Group`.

#### Conclusion:

For the "wait for all goroutines to complete" task, the standard tool is
`sync.WaitGroup`: simple contract, predictable behavior and production
reliability.

#### Example:

```go
var wg sync.WaitGroup

for i := 0; i < 3; i++ {
	wg.Add(1)
	go func(id int) {
		defer wg.Done()
		fmt.Println("worker", id)
	}(i)
}

wg.Wait()
```

</details>


<details>
<summary>33. Why was the pattern `value := value` used in loops and is it relevant after Go 1.22?</summary>

#### Go

The `value := value` template was historically used in `for range` loops to
create a separate local copy of a variable and safely capture it in a closure,
particularly in a goroutine.

#### Why this was needed before Go 1.22:

1. The iteration variable in `range` was actually reused between iterations.

2. A closure would often capture the same variable instead of its "current"
   value.

3. As a result, the goroutine saw unexpected data (usually the last value).

Therefore, they wrote:

`v := v`

to create a new variable within an iteration.

#### What has changed since Go 1.22:

1. The semantics of `range` have been changed: for each iteration, the loop
   variables have separate values to capture in the closure.

2. A typical bug with a "late" value in goroutines has been fixed at the
   language level.

3. In most modern cases, the `value := value` template is no longer needed.

#### Is the template relevant today:

1. **For code guaranteed to work on Go 1.22+** - usually not.

2. **For projects with older versions of Go** - yes, may be necessary.

3. **For mixed environments/libraries** you should aim for the lowest supported
   version.

#### Practical conclusion:

`value := value` was a protective pattern against the specific trap `range`.
After Go 1.22, the need for it mostly disappeared, but it remains relevant in
legacy code or when supporting older versions.

</details>


<details>
<summary>34. Can using goroutines slow down the system and in what cases?</summary>

#### Go

Yes, it can. Despite the lightweight nature of goroutines, they are not "free".
Improper or excessive use of them can reduce performance, increase latency, and
complicate the runtime.

#### When goroutines can slow down the system:

1. **Excessive number of goroutines (goroutine explosion):** thousands or
   hundreds of thousands of tasks without limiting competition put pressure on
   the scheduler and memory.

2. **Fine-grained tasks:** if the work is very small, the startup/coordination
   overhead may be greater than the useful work.

3. **Intensive synchronization:** frequent blocking (`mutex`, channels,
   `select`) creates contention and reduces throughput.

4. **Failed data exchange over channels:** redundant forwarding of large
   payloads or complex fan-in/fan-out topologies can cost more than simpler
   models.

5. **Lack of backpressure:** when producers generate work faster than consumers
   process it, queues accumulate, memory and delays grow.

6. **I/O and external resource issues:** excessive parallelism can overload the
   DB, network, file system, or third-party APIs, degrading the overall system
   rather than speeding it up.

#### How to avoid degradation:

1. Limit competition (worker pool, semaphore, bounded queues).

2. Profile (`pprof`, trace) instead of relying on intuition.

3. Reduce shared mutable state and lock contention.

4. Select the size of parallelism according to the real workload and resources.

#### Conclusion:

Horoutines speed up the system only when parallelism is controlled. In
production, the principle is simple: not "more goroutines", but "enough
goroutines with the right boundaries and synchronization".

</details>


<details>
<summary>35. What is the difference between buffered and unbuffered channels? When is it appropriate to use slice + mutex instead of channels?</summary>

#### Go

Channels in Go can be buffered or unbuffered, and this difference defines the
semantics of synchronization between goroutines. The choice of channel type is a
choice of coordination model, not just a "technical thing".

#### Unbuffered channel (`make(chan T)`):

1. **Synchronous exchange:** `send` is blocked until another goroutine executes
   the corresponding `receive` (and vice versa).

2. **Clear handoff:** is good when tight step synchronization is required.

3. **Queue minimum:** data does not accumulate in the channel.

#### Buffered channel (`make(chan T, n)`):

1. **More asynchronous interaction:** `send` does not block as long as there is
   room in the buffer.

2. **Managed queue:** allows to smooth out short load peaks.

3. **Backpressure due to capacity:** when the buffer is full, `send` blocks
   again.

#### When `slice + mutex` is appropriate instead of channels:

1. **Requires a shared buffer with non-trivial operations:** batch deletion,
   reorder, random access, complex aggregation rules.

2. **When the model is "shared state with explicit lock" and not a message
   flow:** channels are not always the easiest tool for mutable collections.

3. **When subtle memory/layout optimization is important:** `slice` gives more
   direct control over data structure and operations.

4. **When channel architecture creates unnecessary complexity:** sometimes
   `mutex` + a clear invariant is simpler, more readable, and faster.

#### Practical rule of choice:

1. **Channels** — for passing events/messages between independent actor-like
   goroutines.

2. **`slice + mutex`** — for managing a shared collection with a rich set of
   state operations.

#### Conclusion:

Buffered and unbuffered channels differ in the level of exchange synchronicity.
The `slice + mutex` alternative is justified when you want a managed shared
state structure rather than a message transport.

#### Example:

```go
unbuf := make(chan int)    // надсилання чекає отримувача
buf := make(chan int, 100) // надсилання не блокується, поки є місце

buf <- 1
buf <- 2
```

</details>


<details>
<summary>36. What happens when a `nil` channel is read, written, or closed?</summary>

#### Go

A `nil` channel in Go is a channel without initialized internal buffer and
synchronization mechanisms. Its behavior is strictly defined and very important
for competitive logic.

#### Behavior of the `nil` channel:

1. **Reading from `nil`-channel** - blocks forever.

2. **Writing to `nil`-channel** - blocks forever.

3. **Closing the `nil`-channel** - causes panic.

#### Why so:

1. The `nil` channel has no "live" structure through which to exchange.

2. Therefore, send/receive operations cannot complete successfully.

3. `close(nil)` is prohibited, because there is actually nothing to close.

#### Practical consequences:

1. In normal code, a random `nil` channel often leads to a deadlock.

2. In `select` it can be a deliberate tool:

- branch with `nil` channel becomes inactive;

- so dynamically "disable" a specific case without additional flags.

#### Conclusion:

For `nil`-channel send/receive — eternal blocking, and `close` — panic. This
property is both a source of common errors and a powerful `select` control
technique when used deliberately.

</details>


<details>
<summary>37. How and why to use `nil` channels in `select`? Why does the `nil` channel block forever and how to use it?</summary>

#### Go

The `nil` channel in `select` is a controlled way to dynamically enable or
disable individual branches. Since operations on the `nil` channel cannot
complete, the corresponding `case` becomes inactive.

#### Why the `nil` channel blocks forever:

1. The channel is not initialized (`var ch chan T`), that is, it does not have a
   runtime structure for send/receive.

2. `send` and `receive` have no "rendezvous point", so they wait indefinitely.

3. In `select` this means: a case with this channel will never be selected.

#### How to use it in `select`:

1. **Dynamically disable event source:** assign `ch = nil` and branch `case
   <-ch:` is no longer activated.

2. **Lifecycle management of pipeline stages:** after completion of a certain
   stage, the pipeline is reset to exclude it from further selection.

3. **Avoiding redundant state flags:** instead of additional `if` inside the
   loop, the state logic is transferred to the `select` mechanism itself.

#### Practical precautions:

1. If all channels in `select` become `nil` and there is no `default`, you will
   get a permanent lock.

2. `close(nil)` causes panic, so nulling and closing should not be confused.

3. Code with `nil`-channels needs clear invariants, otherwise it is easy to get
   a deadlock that is difficult to debug.

#### Conclusion:

The `nil` channel in `select` is an elegant case activity switch. It is useful
for controlled concurrency logic as long as the states are carefully controlled
and avoid a situation where all paths become deadlocked.

#### Example:

```go
var in <-chan int = source
for {
	select {
	case v, ok := <-in:
		if !ok {
			in = nil // вимикаємо гілку
			continue
		}
		_ = v
	case <-ctx.Done():
		return
	}
}
```

</details>


<details>
<summary>38. When is it appropriate to use `select` with the `default` branch and what scenarios does it cover?</summary>

#### Go

`select` with branch `default` makes the operation non-blocking: if no channel
is ready to be exchanged, control immediately passes to `default`. This is
useful for controlled reactivity, but dangerous when used thoughtlessly.

#### When appropriate:

1. **Try-send / try-receive scenarios:** should try the exchange and, if it is
   not possible now, take an alternative path without blocking.

2. **Event loops with background work:** when, while waiting for events, the
   goroutine should perform auxiliary actions (heartbeat, housekeeping, light
   telemetry).

3. **Backpressure and controlled load shedding:** if the buffer is full,
   `default` can refuse/delay the task instead of blocking the entire loop.

4. **Soft timeouts/status polling:** in combination with `time.Ticker` or other
   logic allows you not to "hang" waiting for a channel.

#### What risks does it cover and create:

1. **Covers the risk of freezing** in critical areas where blocking is
   unacceptable.

2. **But can create a busy loop** (active CPU spinning) if `default` fires too
   often without pause or meaningful work.

#### Practical precautions:

1. Do not use `default` if blocking synchronization is desired.

2. In loops, add pace control (`ticker`, `sleep`, limits) to avoid wasted CPU
   consumption.

3. Clearly fix the policy: what do we do when the channel is not ready (drop,
   retry, queue, log, metric).

#### Conclusion:

`select` from `default` is a non-blocking concurrency tool. It is appropriate
where reactivity and load management are a priority, but requires discipline not
to turn the processing cycle into inefficient active polling.

</details>


<details>
<summary>39. How does `select` work when receiving data from multiple channels at the same time?</summary>

#### Go

If there are multiple `case` ready when `select` is executed, Go chooses one of
them pseudo-randomly. This is done to avoid the rigid priority of the first
branch and to reduce the systematic "starvation" of individual channels.

#### What happens step by step:

1. Runtime checks all `case` in `select`.

2. Defines a set of ready operations (send/receive that can be performed now).

3. If one `case` is ready, it is executed.

4. If several are ready, one is chosen pseudo-randomly.

5. If none are ready:

- executes `default` (if any),

- otherwise `select` is blocked until at least one `case` is ready.

#### Practical consequences:

1. **There is no processing order guarantee** between concurrently ready
   channels.

2. **Cannot encode business priority** only in `case` order in `select`.

3. **The behavior is competitively correct, but non-deterministic**, which is
   normal for event-driven logic.

#### How to implement priority, if it is needed:

1. Build two-phase `select` (critical channel first, then common).

2. Use separate queues/priority scheduler.

3. Enforce an explicit fair/priority policy in the application layer, rather
   than relying on runtime randomization.

#### Conclusion:

If several channels are available at the same time, `select` chooses one
randomly (pseudo-randomly). This is a good strategy for overall fairness, but
prioritization requires explicit architectural logic on top of the basic
`select`.

</details>


<details>
<summary>40. How to safely close a channel in Go if multiple goroutines are writing to it?</summary>

#### Go

Go's basic rule: a channel is closed by **who owns the write side** and only
after all `send` operations are guaranteed to complete. A script with multiple
writer goroutines requires completion coordination.

#### Safe approach (canonical):

1. Start several writer subroutines.

2. Each writer signals about it after completion of work (`WaitGroup.Done()`).

3. A separate control goroutine is waiting for `wg.Wait()`.

4. Only then calls `close(ch)`.

#### Why it's safe:

1. No goroutine writes to the channel after `close`.

2. Avoids panic `send on closed channel`.

3. Closing occurs exactly once per controlled point.

#### What cannot be done:

1. Allow each writer to independently close the shared channel.

2. Close channel "just in case" from multiple locations.

3. Catching panic as a "synchronization mechanism" is an antipattern.

#### Additional practices:

1. For an early stop, use a separate `done/context` rather than `close(dataCh)`
   on the reader side.

2. If you need to guarantee one-time closure in a complex topology, use
   `sync.Once`.

#### Conclusion:

In a multi-writer scenario, the channel is safely closed by the coordinator
after explicitly confirming the completion of all writer subroutines. The
principle is simple: **many senders, one closer, close-after-all-sends**.

#### Example:

```go
ch := make(chan int)
var wg sync.WaitGroup

for i := 0; i < 5; i++ {
	wg.Add(1)
	go func(v int) {
		defer wg.Done()
		ch <- v
	}(i)
}

go func() {
	wg.Wait()
	close(ch) // один координатор закриває канал
}()
```

</details>


<details>
<summary>41. How to implement a semaphore through a buffered channel?</summary>

#### Go

In Go, a semaphore is naturally modeled by a fixed-capacity buffered channel.
The number of slots in the buffer is equal to the maximum allowed number of
simultaneous operations (parallelism).

#### Principle of operation:

1. **Acquire (occupy a slot):** before starting work, the goroutine executes
   `sem <- token`. If the buffer is full, sending is blocked.

2. **Release (release the slot):** after completion, the goroutine executes
   `<-sem`. This frees up space for the next task.

#### Typical form:

- `sem := make(chan struct{}, N)`

- `N` — limit of simultaneously active tasks.

- `struct{}` is chosen as a lightweight token without payload.

#### Why it is effective:

1. **Simple backpressure model:** Redundant tasks naturally wait.

2. **Transparent synchronization:** The Go runtime performs lock/wakeup without
   manual control of conditional variables.

3. **Reads well in the code:** the intention to "restrict competition" is
   immediately apparent.

#### Practical precautions:

1. Always do `release` over `defer` to avoid losing a slot in the event of an
   error.

2. To cancel waiting, use `select` with `context.Done()`.

3. Do not confuse a semaphore (parallelism limit) with a task queue (worker
   pool).

#### Conclusion:

A buffered channel in Go is a canonical implementation of counting semaphore:
simple, reliable, and well integrated into the goroutine model. This is one of
the best ways to control the level of competition in production services.

#### Example:

```go
sem := make(chan struct{}, 10) // максимум 10 одночасних задач

run := func(job Job) {
	sem <- struct{}{}         // зайняти слот
	defer func() { <-sem }() // звільнити слот
	job.Do()
}
```

</details>


<details>
<summary>42. How to implement patterns `Fan-in` and `Fan-out`?</summary>

#### Go

`Fan-out` and `Fan-in` are basic concurrency patterns in Go for managed
parallelism: the former distributes work across multiple executors, the latter
collects results back into a shared thread.

#### `Fan-out` (load branching):

1. There is an incoming problem channel.

2. Starts `N` worker-routine.

3. Each worker reads from a common input channel and processes its part.

#### `Fan-in` (merging results):

1. Several producer-channels or worker-results.

2. Individual merge routines send data to one output channel.

3. After completion of all merge branches, the output channel is closed.

#### Typical architectural scheme:

1. `jobs` channel → `fan-out` on workers.

2. Each worker writes to `results`.

3. `fan-in` aggregates `results` (or several `results`-channels) into one
   channel for the next pipeline stage.

#### Critically important rules:

1. Closing channels should be centralized and one time.

2. Use `WaitGroup` to coordinate worker termination.

3. For early termination, use `context`/`done` to avoid goroutine leaks.

4. Control the size of buffers and level of parallelism to avoid overloading
   memory or external dependencies.

#### Conclusion:

`Fan-out` scales processing, `Fan-in` returns control over the result stream.
Together, they form the basis of most effective pipeline solutions in Go
services.

</details>


<details>
<summary>43. Why should you not use channels to transfer large amounts of data?</summary>

#### Go

Channels in Go are a great tool for coordinating and passing events/small
messages, but not the best transport for massive payloads. For large amounts of
data, they often create unnecessary overhead.

#### Why it might not be effective:

1. **Cost of copying:** passing large values over the channel increases memory
   operations and traffic between goroutines.

2. **Contention and synchronization costs:** channels have internal access
   coordination; at high load it can become a bottleneck.

3. **GC and memory pressure:** large channel buffers or numerous large messages
   increase memory pressure and can increase pauses/runtime costs.

4. **Degradation of cache locality:** large objects pass through the competitive
   pipeline worse than compact signals + access to shared storage.

#### Better alternatives:

1. Transfer over channel **links/handles/indexes**, not big data.

2. Keep the payload in a shared buffer/pool, and use the channel as a ready
   signal.

3. Use a worker pool with controlled access to a shared data structure
   (`slice/map + mutex`) where appropriate.

#### When channels are still appropriate:

1. For small control messages.

2. For events, commands, statuses, and completion signals.

3. For a pipeline where light metadata context moves in the pipeline.

#### Conclusion:

A channel in Go is primarily a synchronization and coordination mechanism. For
large data, it is more efficient to separate: transmit "what to do" through a
channel, and the most massive payloads — through more suitable memory
structures.

</details>


<details>
<summary>44. How to correctly return an error from a goroutine to the main thread?</summary>

#### Go

A routine cannot "return" a value directly via `return` to the caller.
Therefore, the error from the competitive task is transmitted explicitly:
through the error channel or through `errgroup`, which encapsulates this
pattern.

#### Canonical approaches:

1. **`errgroup.Group` + `context` (recommended):** best for running a group of
   goroutines, collecting the first error, and canceling the remaining tasks.

2. **Separate `errCh` + `WaitGroup`:** explicit control over the life cycle;
   after the completion of all workers, the channel is closed, and the main
   thread reads errors.

#### Key rules of correctness:

1. Errors are transmitted in one agreed channel/aggregator.

2. Closing `errCh` is performed by the coordinator after the completion of all
   writer-routines.

3. For the first critical error, other tasks should be stopped through `context`
   (to avoid useless work and goroutine leaks).

4. Errors in competing branches cannot be ignored - this creates "silent"
   defects.

#### Typical processing strategy:

1. Start workers with access to `ctx`.

2. On error, send `error` to the aggregator.

3. Cancel context (if fail-fast policy is required).

4. Wait for all goroutines to complete.

5. Return the agreed result (first error or aggregated error).

#### Conclusion:

Correct error "return" from goroutine is discipline of explicit communication
channel plus lifecycle management via `WaitGroup`/`errgroup` and `context`. In
production, most often the optimal choice is `errgroup`.

#### Example (Go 1.22+):

```go
g, ctx := errgroup.WithContext(context.Background())

for _, task := range tasks {
	g.Go(func() error {
		return task.Run(ctx)
	})
}

if err := g.Wait(); err != nil {
	return err
}
```

</details>


<details>
<summary>45. Can `defer` in Go catch a (`recover`) panic that occurred in a child goroutine?</summary>

#### Go

Short answer: **no**. `recover` only works in the same goroutine where the panic
occurred, and only in a `defer` function executing in its call stack.

#### The main rule:

1. Panic does not "fly" between goroutines as a controlled signal for `recover`.

2. `defer` in the parent goroutine cannot catch the panic of the child.

3. In order to catch a panic in a worker-routine, `defer` with `recover` must be
   inside this particular worker-routine.

#### Practical consequences:

1. If panic in the child goroutine is not caught locally, the process may crash.

2. For stable services, each "risky" goroutine is wrapped with a protective
   `defer func(){ if r := recover(); r != nil { ... } }()`.

3. After `recover` it is necessary to clearly signal a failure to the main
   circuit (via `error`-channel, `errgroup`, metrics, logging).

#### What is considered good practice:

1. Local `recover` at the launch point of long-lived workers.

2. Clear policy: panic turns into an error/alert and doesn't go away silently.

3. Using `context` for coordinated termination of other goroutines after a
   critical failure.

#### Conclusion:

`recover` in Go has a local scope — a single goroutine. Therefore, panic
interception in competing code must be designed at the level of each child
goroutine separately.

</details>


<details>
<summary>46. Talk about concurrency patterns in Go.</summary>

#### Go

Concurrency patterns in Go are repetitive architectural patterns for
coordinating goroutines, pipes, and synchronization primitives. Their goal is to
provide manageable parallelism without chaos, leaks, and deadlocks.

#### The most used patterns:

1. **Worker Pool**

- a fixed number of worker-routines reads tasks from the queue;

- limits the level of parallelism and stabilizes the load.

2. **Fan-out / Fan-in**

- `fan-out`: allocation of one queue of tasks to many executors;

- `fan-in`: Merging results from multiple sources into one channel.

3. **Pipeline (conveyor of stages)**

- data goes through successive stages of processing;

- each stage can have its own competition and backpressure.

4. **Semaphore via buffered channel**

- limits the number of simultaneous operations;

- useful for working with databases, file descriptors, external APIs.

5. **Context cancellation**

- centralized cancellation of the entire group of goroutines;

- prevents leaks on timeout, error, or shutdown.

6. **Errgroup (fail-fast orchestration)**

- collects errors from a group of tasks;

- combines conveniently with `context` to stop the rest of the work early.

7. **Single owner / Actor-like loop**

- one goroutine has mutable state;

- others interact via messages, reducing lock contention.

8. **Publish/Subscribe (broadcast)**

- events are sent to multiple consumers;

- requires careful monitoring of buffers and subscriber lifecycle.

#### Critical principles for all patterns:

1. Explicit resource ownership and channel closing rules.

2. Contest restrictions (not "infinite" goroutines).

3. Required termination path (`context`, `done`, `WaitGroup`).

4. Observability: metrics, logging, profiling.

#### Conclusion:

The power of Go is not in "the goroutines themselves", but in the discipline of
patterns. It is the right combination of worker-pool, pipeline, fan-in/fan-out,
cancellation and error-coordination that gives systems scalability,
predictability and production reliability.

</details>


<details>
<summary>47. When to use `sync.Mutex` and when to use `sync.RWMutex`?</summary>

#### Go

`sync.Mutex` and `sync.RWMutex` solve the same problem — protecting shared
state, but with a different concurrency model. The right choice depends on the
profile of data access: the ratio of reads and writes, the duration of critical
sections and the level of contention.

#### `sync.Mutex` — when to choose:

1. **Mixed or frequent writes:** unless write operations are infrequent, the
   benefit of `RWMutex` is often negated.

2. **Short critical sections:** simple lock/unlock usually gives predictable and
   fast behavior.

3. **Basic default choice:** less complexity, less chance to get the lock model
   wrong.

4. **When ease of maintenance is important:** `Mutex` is easier to read, debug,
   and profile.

#### `sync.RWMutex` — when it makes sense:

1. **Reads dominate, writes are rare:** many concurrent readers can work in
   parallel.

2. **Reads are relatively long:** parallel read-access gives a real gain in
   throughput.

3. **Read contention is high:** and there is empirical evidence that it is the
   read-lock that becomes the bottleneck.

#### Important notices:

1. `RWMutex` is not "automatically faster" - due to more complex internal
   coordination, it may be slower in real workloads.

2. Readers are still blocked during frequent write operations.

3. The final choice should be made based on profiling (`pprof`, benchmarks), not
   intuition.

#### Rule of thumb:

1. Start with `sync.Mutex`.

2. Go to `sync.RWMutex` only when there is a measured read-heavy scenario and a
   proven performance gain.

#### Conclusion:

`sync.Mutex` is a reliable default for most tasks. `sync.RWMutex` is a point
optimization tool for reader-oriented workloads, where the gain is confirmed by
metrics.

</details>


<details>
<summary>48. Why can't `sync.Mutex` objects be copied?</summary>

#### Go

`sync.Mutex` contains the internal lock state. After the first use, copying such
an object creates a dangerous situation: two different instances of the lock
state appear, which the programmer can mistakenly perceive as one.

#### Why it is essentially prohibited:

1. **Mutex is not just "data", but a stateful synchronization primitive.**

2. **The copy does not share the same lock-state** with the original.

3. This breaks mutual exclusion guarantees and can lead to race, deadlock, or
   panic in complex scenarios.

#### Typical ways to accidentally copy a mutex:

1. Pass a structure with `sync.Mutex` by value to a function.

2. Return the following structure by value after initialization/use.

3. Keep/forward copies via channels or value collections.

#### Correct practice:

1. Structures from `sync.Mutex` should be used via pointers (`*T`), not
   value-copy.

2. Do not export `Mutex` directly in the public API.

3. If the type has a lock, document that it is not copied after the first use.

4. Use `go vet` (copylocks) and linters for early detection.

#### Conclusion:

`sync.Mutex` cannot be copied because it undermines the synchronization model
itself. Remember the rule: lock primitives have a stable identity and must live
in one instance per protected state.

</details>


<details>
<summary>49. Why is reading and writing shared state without synchronization a data race, even if "logically safe"?</summary>

#### Go

In terms of the Go memory model, `data race` occurs when two or more goroutines
simultaneously access the same variable, at least one of which is a write
operation, and there is no established `happens-before` relationship (i.e.
synchronization) between these accesses.

#### Why "logically safe" does not save:

1. **Logic in the developer's head ≠ memory model guarantee.** Without
   synchronization, the order of visibility of records between cores/threads is
   not defined.

2. **Compiler and CPU optimizations can change the observed order** of
   reads/writes within the allowed memory model.

3. **Instability under load:** code may "work" in local startup, but break in
   production or CI.

#### What are the consequences of race:

1. Reading outdated or partially updated values.

2. Irreproducible bugs (heisenbugs) that are difficult to debug.

3. Violation of business state invariants without explicit panic.

#### What is considered correct synchronization:

1. `sync.Mutex` / `sync.RWMutex`

2. Atomics (`sync/atomic`) for simple low-level scenarios

3. Channels as ownership/signalling mechanism

4. `WaitGroup`, `Cond`, `Once`, `context` — in their coordination roles

#### Conclusion:

Without synchronization, shared read/write in Go is a race by definition,
regardless of subjective "logical safety". The only reliable way is to
explicitly form the `happens-before` relationship through the correct
concurrency primitives.

</details>


<details>
<summary>50. What is Race Condition and how does the `-race` detector work? What it can and cannot detect?</summary>

#### Go

`Race Condition` is a general class of concurrency defects where the result of a
program depends on an unpredictable order of events between threads of
execution. `Data race` is a special case of the race condition, which refers to
dangerous simultaneous access to the same memory without synchronization.

#### How `-race` works:

1. During `go test -race` / `go run -race` code is instrumented.

2. Runtime tracks memory reads/writes between goroutines.

3. If accesses without `happens-before` are detected (and there is a record) —
   `data race` with stack traces is reported.

#### What `-race` detects well:

1. Classic read/write and write/write races on shared variables.

2. Missed lock/unlock in competitive areas.

3. Part of coordination errors in test scenarios with real competition.

#### What `-race` does not guarantee:

1. **Does not detect all race conditions as logical bugs:** eg, incorrect
   interaction protocol without direct data race.

2. **Doesn't see unexecuted code:** if tests don't cover a competitive path,
   race may go unnoticed.

3. **Does not prove bug-free:** A "clean" run means only that the tool did not
   detect any violations during that run.

4. **Has overhead:** slowdown and increased memory consumption in
   instrumentation mode.

#### Practical conclusion:

`-race` is a mandatory tool for competing code hygiene, but not an absolute
oracle of correctness. Its power is revealed in combination with quality tests,
design invariants, and synchronization discipline.

</details>


<details>
<summary>51. What are the advantages of atomic operations compared to mutex for simple competitive operations?</summary>

#### Go

`atomic` operations in Go are appropriate for very simple competitive scenarios
where you need to safely perform an elementary operation on a single value
(increment, read a flag, CAS). In such cases, they may be lighter than `mutex`.

#### Advantages of the atomic approach:

1. **Less overhead for simple operations:** no explicit `Lock/Unlock` around the
   short operation.

2. **High efficiency in hot-path counters and flags:** eg metrics, stop/start
   states, lightweight coordination.

3. **No locking in the classical sense:** threads do not need to wait for a lock
   owner for atomic read/write.

4. **Clear memory-order guarantees via API `sync/atomic`:** correct visibility
   between goroutines for a specific variable is ensured.

#### When atomic is better than mutex:

1. Operation applies to **one** variable or very local state.

2. The logic is simple and well formalized (`Load`, `Store`, `Add`,
   `CompareAndSwap`).

3. Requires minimum latency in the high-frequency path.

#### When mutex is better:

1. A **invariant between multiple fields** must be protected.

2. The operation includes several steps with domain logic.

3. Readability and maintainability are more important than micro-optimization.

#### Important notice:

Atomic is not a universal replacement for `mutex`. Excessive use of atomics
complicates the code and increases the risk of subtle bugs in the memory model.

#### Conclusion:

The advantage of atomic operations is fast, low-cost synchronization for simple
cases. For complex shared state and business invariants, `mutex` is usually the
more reliable tool.

</details>


<details>
<summary>52. How does `sync.WaitGroup` work and what will happen with a negative counter? Why can't `wg.Done()` be called before `wg.Add()`?</summary>

#### Go

`sync.WaitGroup` is a counter of active concurrent tasks. Its purpose is to
allow one goroutine (`Wait`) to wait for the others to complete their work.

#### How it works:

1. `wg.Add(n)` increases the counter by `n` (we add the number of tasks).

2. Each completed task triggers `wg.Done()` (equivalent to `Add(-1)`).

3. `wg.Wait()` is blocked until the counter reaches zero.

#### What will happen with a negative counter:

1. This is a logical coordination error.

2. Runtime causes panic (typically: `sync: negative WaitGroup counter`).

3. This situation means that `Done()` was called more times than `Add()` was.

#### Why you can't do `Done()` to `Add()`:

1. The task lifecycle contract is being violated.

2. `Wait()` may end prematurely, because at the moment of waiting, the counter
   does not yet reflect the real number of jobs.

3. In the worst case, we will get a negative counter and panic.

#### Correct discipline:

1. Call `Add(1)` **before** the goroutine starts.

2. Inside the goroutine, set `defer wg.Done()` immediately at the entrance.

3. Call `Wait()` only after registering all tasks.

#### Conclusion:

`WaitGroup` is only reliable under strict `Add -> go -> Done -> Wait` sequence.
A negative counter and `Done()` to `Add()` is a signal of a broken
synchronization model, which inevitably leads to unstable behavior or panic.

#### Example:

```go
var wg sync.WaitGroup
wg.Add(1)

go func() {
	defer wg.Done()
	work()
}()

wg.Wait()
```

</details>


<details>
<summary>53. What is the difference between `sync.WaitGroup` and `errgroup.Group`? When to use each?</summary>

#### Go

`sync.WaitGroup` and `errgroup.Group` both coordinate the completion of
goroutines, but they have different levels of abstraction: `WaitGroup` only
waits, while `errgroup` additionally handles errors and cancellation via
`context`.

#### `sync.WaitGroup`:

1. Only responsible for waiting for tasks to complete.

2. Does not collect errors out of the box.

3. Does not cancel other goroutines automatically.

4. Requires manual infrastructure:

- error channel;

- coordination `context`;

- fail-fast logic.

#### `errgroup.Group`:

1. Allows you to run goroutines through `Go(func() error)`.

2. Returns the first error received in `Wait()`.

3. Paired with `errgroup.WithContext` automatically cancels context on error.

4. Reduces boilerplate for the typical "parallel tasks + stop on error" pattern.

#### When to choose `WaitGroup`:

1. Just wait for completion without error-aggregation.

2. The error handling policy is non-standard and completely custom.

3. Low-level control is more important than API convenience.

#### When to choose `errgroup`:

1. Needs a clear "failure in one task → stop the rest" model.

2. Need to quickly and cleanly implement competitive orchestration.

3. Readability and short, maintainable code are important.

#### Conclusion:

`WaitGroup` - "wait only" synchronization primitive. `errgroup` - higher level:
"wait + return an error + cancel the rest via context". For most production
scenarios with errors and fail-fast semantics, `errgroup` is more practical.

</details>


<details>
<summary>54. Describe the purpose and implementation of `sync.Once` - how does it guarantee one-time initialization?</summary>

#### Go

`sync.Once` is intended for guaranteed one-time execution of a function under
conditions of concurrent access. Regardless of the number of goroutines calling
`once.Do(f)` at the same time, the body of `f` must be executed only once.

#### What is it used for:

1. Lazy initialization of singleton resources.

2. One-time configuration/cache loading.

3. Safely run heavy initialization without duplicating work.

#### How `sync.Once` guarantees reproducibility:

1. Checks an internal done/failed status flag.

2. If the initialization has not been done yet — blocks competitors
   synchronously.

3. Exactly one goroutine executes `f`.

4. On success marks the state as "done" and further `Do` returns without
   restarting `f`.

#### Important properties:

1. The correct visibility of initialized data for other goroutines is guaranteed
   (memory-safety through internal synchronization).

2. Other goroutines that came during `f` execution will wait for completion.

3. `Once` is not intended to be "restarted" - it is a one-time life cycle.

#### Nuances and warnings:

1. If `f` panics, the behavior needs careful design consideration: `Once` is not
   a fallback mechanism.

2. You should not hide too complex business logic in `Do`; it is better to keep
   the initialization of the resource there.

3. Reset/reload tasks require other patterns (atomic pointer, mutex, versioned
   state, etc.).

#### Conclusion:

`sync.Once` is a disciplined one-time initialization primitive: race-safe,
predictable, and very useful where rerunning initialization is either redundant
or dangerous.

</details>


<details>
<summary>55. What is `sync.Cond` and when does it override a channel?</summary>

#### Go

`sync.Cond` is a conditional synchronization primitive: it allows goroutines to
wait until a certain state (condition) becomes true and be woken by a signal
from another goroutine.

#### Base model `sync.Cond`:

1. `Cond` works on top of `Locker` (usually `*sync.Mutex`).

2. The routine in the loop checks the condition under lock.

3. If the condition is false — calls `Wait()`.

4. Another goroutine calls `Signal()` or `Broadcast()` after a state change.

#### Key methods:

1. **`Wait()`** — atomically releases the lock, falls asleep, and after waking
   up grabs the lock again.

2. **`Signal()`** — wakes up one waiting goroutine.

3. **`Broadcast()`** - wakes up all expectants.

#### When `sync.Cond` channel prevails:

1. **Complex condition on shared state, not message transfer:** when it is
   important to wait for "predicate over state" and not receive payload.

2. **Many waiters on one lock-protected resource:** `Cond` more naturally
   expresses coordination around shared state.

3. **Fine wake-up control required:** `Signal/Broadcast` are sometimes better
   suited than channel semantics.

4. **High-frequency scenarios with minimal allocation noise:** in certain
   low-level cases, `Cond` gives a more efficient model than building additional
   channel protocols.

#### When the channel is better:

1. When the task is to transfer event/data between independent actors.

2. When a simple pipeline model and a readable message flow are important.

3. When you don't want to manage the shared mutable state under lock.

#### Conclusion:

`sync.Cond` is a "waiting for mutex condition to change" tool, while a channel
is a "passing message" tool. `Cond` prevails where the center of the logic is
the state itself and its invariants, not the data transport.

</details>


<details>
<summary>56. How is `sync.Map` arranged, when does it give better performance compared to map + mutex, and where is it used in the standard library?</summary>

#### Go

`sync.Map` is a specialized competitive map from the `sync` package, optimized
primarily for read-heavy workloads and scenarios where keys are read frequently
and rarely changed.

#### How `sync.Map` is arranged conceptually:

1. Has a two-layer access model:

- **read-part** for fast, mostly lock-free readings;

- **dirty-part** for updates and new entries under sync.

2. Reading from a "hot" read zone often does without a common mutex, which
   reduces contention.

3. Inter-layer writes/promotions have more complex internal logic, but are aimed
   at not penalizing bulk reads.

#### When `sync.Map` can be faster than `map + mutex`:

1. **Many reads, few writes** (classic read-mostly workload).

2. **Keys mostly stable**, without aggressive churn.

3. **Highly competitive read access** from many goroutines.

#### When more is better `map + mutex`:

1. Entries are many or dominate.

2. Requires complex invariants over multiple keys.

3. Type safety is more important (because `sync.Map` works through `any`).

4. Needs simpler and more obvious logic for the team to support.

#### Where used in the standard library:

`sync.Map` is used in internal caches and tables where the nature of access is
close to read-heavy (in particular, in parts of the runtime/standard packages
for caching metadata and auxiliary structures). The key idea is the same
everywhere: minimize blocking on bulk reads.

#### Conclusion:

`sync.Map` is not a "best map overall", but a point tool for a specific load
profile. If you have a read-mostly scenario with high competition, it can give a
win; in other cases, simple `map + mutex` is often more transparent and
efficient.

</details>


<details>
<summary>57. What are concurrency tests in Go and why are they used?</summary>

#### Go

Concurrency tests in Go are tests that test the behavior of code under
conditions of parallel execution of goroutines, state sharing, and resource
competition. Their goal is to detect defects that do not appear in a linear
scenario.

#### What exactly do the following tests check:

1. Correctness of synchronization (`mutex`, `channel`, `atomic`, `WaitGroup`).

2. Lack of data race in shared state.

3. Resistance to deadlock/live-lock scenarios.

4. Correct completion of goroutines (no leaks).

5. Observance of invariants under competitive load.

#### Why are they needed:

1. **Early detection of competitive bugs:** many of them only show up under
   parallelism pressure.

2. **Decreasing flaky behavior in production:** tests capture scenarios where
   the order of events is non-deterministic.

3. **Assertion of architectural guarantees:** such as that the system does not
   lose events and does not violate state consistency.

4. **Safer refactoring:** competitive invariants remain protected by the
   regression set.

#### Tools and Practices in Go:

1. `go test -race` as a mandatory verification level.

2. Parallel scripting via goroutines, `t.Run`, `t.Parallel`.

3. Explicit timeouts/`context` to prevent tests from hanging.

4. Stress runs and multiple runs to increase the chance of reproducing
   non-deterministic errors.

#### Conclusion:

Concurrency tests are not an "extra luxury", but a necessary element of quality
for Go services. They check not only the functionality, but also the correctness
of the interaction of goroutines in real conditions of parallelism.

</details>


<details>
<summary>58. Why does Go use `context.Context` and how is it passed through the function call tree?</summary>

#### Go

`context.Context` in Go is a standard mechanism for managing the
request/operation lifecycle: cancellations, deadlines, timeouts, and request
metadata. It allows all branches of execution to see a single "stop" signal.

#### Why do you need `Context`:

1. **Cancellation:** stop work that is no longer needed (the client has
   disconnected, an error has occurred in a nearby branch, the service is
   terminating).

2. **Deadline/timeout:** limit the execution time of operations (HTTP, DB,
   external APIs) so as not to hang indefinitely.

3. **Request-scoped values:** transfer service request data (trace-id,
   auth-token, tenant-id) between layers.

#### How it is passed through the call tree:

1. `ctx` is passed as the **first parameter** to a function that can block or do
   I/O.

2. Each child call receives the same `ctx` or derivative:

- `context.WithCancel`

- `context.WithTimeout`

- `context.WithDeadline`

- `context.WithValue`

3. Child contexts form a tree:

- canceling a parent context cancels all children;

- deadlines are inherited (or narrowed).

#### Practical rules:

1. Do not store `Context` in a structure as a long-lived field.

2. Do not pass `nil` context (use `context.Background()` or `context.TODO()`).

3. Do not use `WithValue` for business parameters that must be explicit function
   arguments.

#### Conclusion:

`context.Context` is the query "nervous system" in Go. It spreads timing and
cancellation control throughout the call tree, making competing code manageable,
economical, and predictable in a production environment.

#### Example:

```go
func handler(w http.ResponseWriter, r *http.Request) {
	ctx := r.Context()
	if err := service.Do(ctx); err != nil {
		http.Error(w, err.Error(), 500)
	}
}

func (s *Service) Do(ctx context.Context) error {
	ctx, cancel := context.WithTimeout(ctx, 2*time.Second)
	defer cancel()
	return s.repo.Call(ctx)
}
```

</details>


<details>
<summary>59. Is `context.Context` immutable and what does it mean in practice?</summary>

#### Go

Yes, `context.Context` is conceptually immutable: after creation, the existing
context is not "edited", but a new derivative context is built on top of the
parent one.

#### What does immutable mean in the case of `Context`:

1. Calls `WithCancel`, `WithTimeout`, `WithDeadline`, `WithValue` do not change
   the old `ctx`.

2. They return a **new** descendant context.

3. The parent context remains as it was before.

#### Practical consequences:

1. **Safe propagation between goroutines:** the same `ctx` can be passed around
   without the risk of "hidden overwriting" of parameters.

2. **Transparent Lifecycle:** The context tree clearly shows who inherited
   cancel/deadline from whom.

3. **Intended API behavior:** a function that received `ctx` cannot sneakily
   "twist" it for other calls; it can only create a local descendant.

4. **Better testability and debugging:** it's easier to trace exactly where
   timeout/cancel/value appeared, because they are separate derived nodes, not
   mutations of a single object.

#### Important clarification:

Immutability does not mean that there is no dynamics inside: the cancel signal
and the deadline state can change over time. But this is a change of the
**execution state** within the context model, not an "in-place" mutation of the
API contract of the passed object.

#### Conclusion:

`context.Context` in Go is a functional-chain model: we do not change the
existing one, but create a derivative. This gives clean composition, secure
concurrency, and predictable query lifecycle management.

</details>


<details>
<summary>60. How does using `context.WithCancel` help avoid goroutine leaks?</summary>

#### Go

`context.WithCancel` gives a managed termination signal to all goroutines
running within the same context tree. This is the key to preventing goroutine
leak — a situation where auxiliary goroutines remain "alive" after the work has
lost its relevance.

#### How a goroutine leak occurs:

1. The routine is waiting for a channel/network/timer without a stop condition.

2. The request has already ended or has become unnecessary, but the worker did
   not know about it.

3. Such "orphaned" goroutines accumulate and consume resources.

#### Role `WithCancel`:

1. Creating child context: `ctx, cancel := context.WithCancel(parent)`.

2. All worker goroutines have `select` with branch `case <-ctx.Done():`.

3. When `cancel()` is called, all dependent goroutines receive a stop signal.

4. Groutines terminate in a controlled manner, freeing resources.

#### Practical safety rules:

1. Always call `cancel()` (often through `defer cancel()`), even on successful
   completion.

2. In every long-lived loop/blocking operation, check `ctx.Done()`.

3. Skip `ctx` through all I/O calls that support cancellation.

4. Combine with `WaitGroup`/`errgroup` to wait for actual completion.

#### What it gives the system:

1. Absence of "hanging" background workers.

2. Better CPU/Memory utilization under load.

3. Predicted shutdown and more stable behavior of the service.

#### Conclusion:

`context.WithCancel` is the basic anti-leak mechanism in Go concurrency: a
single explicit stop signal that terminates all related goroutines in a
consistent manner and saves the system from resource bloat.

</details>


<details>
<summary>61. Why does Go use non-standard key types (eg `struct{}`) for `context.WithValue` and how does this prevent collisions?</summary>

#### Go

In `context.WithValue`, the key must be comparable, but most importantly, it
must be **unique within your application and dependency space**. That is why it
is recommended to use your own (non-standard) key types instead of the commonly
used `string`.

#### Why `string` keys are dangerous:

1. Different packages may accidentally use the same string (`"userID"`,
   `"request_id"`, etc.).

2. The value in the context will be overwritten or "shadowed" by another
   package.

3. Get silent, hard-to-reproduce routing/authentication/login errors.

#### How a non-standard type prevents collisions:

1. Creates a private key type in the package, for example: `type ctxKey
   struct{}` or `type ctxKey int`.

2. External code cannot accidentally use the same key type and value.

3. This way the key namespace becomes isolated at the level of the typical
   system.

#### Why `struct{}` is often taken:

1. Lightweight marker type without payload.

2. Emphasizes that the identity of the key is important, not its "data".

3. Corresponds well with the "package-local unique key" idiom.

#### Rule of thumb:

1. Declare keys as non-exported package variables.

2. Do not use "empty" strings as keys for `WithValue`.

3. Store in `Context` only request-scoped service data, not business parameters.

#### Conclusion:

Non-standard key types in `context.WithValue` are a type-safe namespace
mechanism. They reliably reduce the risk of collisions between packages and make
contextual values ​​predictable in large codebases.

#### Example:

```go
type requestIDKey struct{}

func withRequestID(ctx context.Context, id string) context.Context {
	return context.WithValue(ctx, requestIDKey{}, id)
}

func requestID(ctx context.Context) (string, bool) {
	v, ok := ctx.Value(requestIDKey{}).(string)
	return v, ok
}
```

</details>


<details>
<summary>62. What is the difference between `context.Value` and passing parameters via function arguments?</summary>

#### Go

`context.Value` and normal function arguments have different purposes. In a
competent Go design, they are not interchangeable: arguments convey business
data, and `context.Value` is a service request-scoped metacontext.

#### Pass through arguments:

1. **Explicit API contract:** all required data is visible in the signature.

2. **Type safety and readability:** the compiler helps control correctness.

3. **Best choice for domain logic:** domain parameters must be passed directly.

#### `context.Value`:

1. **Implicit service data channel:** trace-id, request-id, auth-claims, tenant,
   correlation metadata.

2. **Propagates through layers without inflating signatures:** useful for
   middleware, logging, observability.

3. **Less transparency:** value dependency not obvious from function signature.

#### Why you should not replace the `context.Value` arguments:

1. API clarity is falling ("hidden" inputs appear).

2. Increases the risk of runtime errors due to assertion with `any`.

3. Tests and refactoring are complicated.

#### Rule of thumb:

1. In `Context` is only what belongs to the request lifecycle and is needed by
   the infrastructure layers.

2. In the function parameters - everything that is the essence of the business
   operation.

#### Conclusion:

Arguments form an explicit domain contract; `context.Value` carries the service
metadata of the request. Mixing these roles degrades the architecture, so
professional Go code keeps the line between them clear.

</details>


<details>
<summary>63. How does Stack vs Heap allocation work in Go?</summary>

#### Go

In Go, the placement of data in the Stack or Heap is determined by the compiler
through escape analysis. The developer does not choose this manually directly,
but can write code to reduce unnecessary heap allocations.

#### Stack allocation:

1. Data lives within a function call (or a managed goroutine stack).

2. Allocation and release are very cheap.

3. Does not directly load the GC.

#### Heap allocation:

1. Data is required outside the current stack frame.

2. Memory is managed by the garbage collector.

3. Gives higher overhead (allocation + subsequent garbage collection).

#### What decides where the value goes:

1. **Escape analysis of the compiler:** if the value "escapes" outside the
   function (pointer is returned, stored in a long-lived structure, closure is
   captured, etc.), it gets into the Heap.

2. **Usage context:** even a local variable can end up on the Heap if its
   lifetime is longer than the current frame.

#### Why this is important:

1. More Heap allocations = more work for the GC.

2. In hot-path, it affects latency and throughput.

3. Optimizing allocations often gives a noticeable increase in service
   performance.

#### Practical conclusion:

In Go, the key is not to "manually manage memory", but to understand escape
behavior. Clear data design and minimization of unnecessary leaks in Heap help
to write fast and stable production code.

</details>


<details>
<summary>64. How to minimize heap allocations with `sync.Pool`?</summary>

#### Go

`sync.Pool` is a temporary object reuse mechanism that allows you to reduce the
frequency of heap allocations in hot code areas. The idea is simple: not to
create short-lived objects anew every time, but to take them from the pool and
return them after use.

#### Basic scheme:

1. Create a pool of `New` that initializes the object as needed.

2. At the input of the operation: `obj := pool.Get()`.

3. Before use, bring the object to a valid state.

4. After completion: clear fields and `pool.Put(obj)`.

#### Why this reduces allocations:

1. Part of requests receives already allocated objects.

2. Fewer new Heap allocations.

3. Less pressure on GC with high frequency of short operations.

#### Where `sync.Pool` is particularly relevant:

1. Buffers (`[]byte`, `bytes.Buffer`) in serialization/network handlers.

2. Temporary auxiliary structures in parse/encode/decode paths.

3. Highly loaded HTTP/RPC services with repeated short operations.

#### Important notices:

1. `sync.Pool` is a cache, not long-term storage; elements can be cleaned by GC.

2. The object before `Put` must be brought to a clean state, otherwise data
   leakage between requests is possible.

3. Pool is not a panacea: on cold paths, the complexity of the code may not pay
   off.

4. Optimization should be confirmed by profiling, not intuition.

#### Conclusion:

`sync.Pool` is effective for reusing short-lived objects in hot paths where
critical allocations and GC-pause are critical. Its strength lies in reducing
allocation turbulence, but it should be applied selectively and profiled.

</details>


<details>
<summary>65. What do the `GOGC` and `GOMEMLIMIT` environment variables mean and how do they affect the garbage collector?</summary>

#### Go

`GOGC` and `GOMEMLIMIT` are key parameters to control GC behavior in Go. They
allow you to balance memory consumption, garbage collection frequency and
service performance.

#### `GOGC`:

1. Specifies the target heap growth rate before the next GC cycle (in percent).

2. Typical value is `100` (allow the heap to roughly double relative to "live"
   data after the previous GC).

3. More `GOGC`:

- less GC cycles;

- more memory consumption;

- potentially lower GC CPU overhead.

4. Less than `GOGC`:

- more frequent GC;

- smaller heap;

- higher assembly overhead.

#### `GOMEMLIMIT`:

1. Sets a soft upper memory limit within which the runtime tries to keep the
   process.

2. When memory approaches this limit, the GC works more aggressively, even if
   `GOGC` a less frequent collection would allow.

3. Especially useful in containers/orchestrators with hard memory limits.

#### How they work together:

1. `GOGC` sets the general "greedyness" of heap growth.

2. `GOMEMLIMIT` acts as a fuse that limits excessive memory growth.

3. In production, it is the combination of both parameters that gives the best
   control of latency and OOM risks.

#### Practical approach:

1. Start with defaults.

2. Measure `heap`, GC pause, CPU, tail-latency under real load.

3. Tune parameters gradually, capturing impact on SLA.

4. For containers, it is necessary to match `GOMEMLIMIT` with the platform
   memory-limit.

#### Conclusion:

`GOGC` controls the GC frequency through the heap growth target, and
`GOMEMLIMIT` limits memory from above. Together, they form a practical tool for
fine-tuning the runtime behavior of Go services.

</details>


<details>
<summary>66. What is `runtime.SetFinalizer` and is it used in the standard library?</summary>

#### Go

`runtime.SetFinalizer` is a mechanism for binding a finalizer function to an
object that can be called by the GC before the object is finally freed.
Important: The finalizer does not provide strict runtime guarantees and is not a
reliable replacement for explicit `Close`/`Dispose`.

#### What `SetFinalizer` does:

1. Registers a callback for a specific heap object.

2. When an object becomes unreachable, the runtime **may** run a finalizer.

3. The object will then be collected in one of the next GC cycles.

#### Key limitations:

1. **There is no guarantee "when" the finalizer will run.**

2. **There is no guarantee that it will execute before the process completes.**

3. Finalizers complicate lifecycle reasoning and can create hidden costs/delays.

#### Rule of thumb:

1. For resources (files, sockets, handles, external connections), always use an
   explicit closure (`defer obj.Close()`).

2. The finalizer is only allowed as a "safety net" against usage errors, not the
   primary way to control the resource.

#### Whether used in the standard library:

Yes, used pointwise in some low-level places as an auxiliary security/diagnostic
mechanism, but not as the underlying resource management model. The general
philosophy of the standard library is an explicit lifecycle and explicit
closure.

#### Conclusion:

`runtime.SetFinalizer` is a specialized tool with soft guarantees. In
production-Go, it is used carefully and rarely; explicit resource management
remains the foundation of reliable code.

</details>


<details>
<summary>67. How to find a memory leak with `pprof`?</summary>

#### Go

Searching for memory leaks in Go through `pprof` is based on comparing heap
profiles over time: if "live" objects grow steadily without returning to the
base level, we have a sign of a leak or uncontrolled reference retention.

#### Basic diagnostic strategy:

1. Enable profiling (`net/http/pprof`) in the service.

2. Remove multiple heap profiles:

- at the start;

- under workload;

- after a "quiet" period.

3. Compare profiles (`go tool pprof`, diff-mode) to find types/stacks that keep
   growing.

#### What to watch in `pprof`:

1. **`inuse_space` / `inuse_objects`** — that really remains in memory.

2. **Top allocators** and their call stacks.

3. **The call graph (`web`)** is where long-lived objects are kept.

4. Dynamics after several GC cycles: the real leak does not "blow up".

#### Typical sources of leaks:

1. Global map/cache without eviction policy.

2. Uncleared buffers/queues/channels.

3. Non-terminating routines that hold references to large structures.

4. Failed to project pools or "forever" metric/label collections.

#### Practical techniques:

1. Run profiles under a representative workload.

2. Add comparison snapshots before/after fix.

3. Watch the goroutine profile in parallel (`goroutine`) — goroutine leaks often
   correlate with memory leaks.

#### Conclusion:

`pprof` allows you to find a memory leak not "by eye", but demonstrably: due to
the growth of `inuse` metrics and specific retention stacks. The key to success
is the time profile comparison in a stable, reproducible load.

</details>


<details>
<summary>68. How to find hot paths and measure throughput?</summary>

#### Go

`Hot paths` are code sections where the program spends the most time or
resources. To find them correctly, you need not intuition, but profiling under
real or close to real load.

#### How to find hot paths:

1. **CPU Profiling (`pprof`):** shows where CPU time is spent the most.

2. **Heap/alloc-profiles:** help to find "hot" allocation paths that often cause
   indirect degradation through GC.

3. **Trace (`go tool trace`):** gives a picture of the scheduler, locks, delays
   between goroutines and I/O.

4. **Flame graph / top / call graph:** visualize which functions form the main
   cost.

#### How to measure throughput:

1. Define bandwidth business metrics:

- req/s, msg/s, jobs/s, rows/s, etc.

2. Conduct controlled load testing:

- fixed input;

- known competitive profile;

- stable startup environment.

3. Remove metrics simultaneously:

- throughput;

- latency (p50/p95/p99);

- CPU, memory, GC, lock contention.

4. Compare "before/after" changes under the same conditions (and preferably with
   multiple runs).

#### Practical principles:

1. Optimize only what is confirmed by the profiler.

2. Do not improve throughput at the cost of uncontrolled growth of tail-latency.

3. After optimization, re-profile to ensure that the bottleneck is indeed gone
   and not shifted.

#### Conclusion:

Finding hot paths and measuring throughput is a single cycle: **profiling →
hypothesis → change → repeat measurement**. In Go, this approach is well
supported by the standard tooling and gives engineering sound results.

</details>


<details>
<summary>69. How to optimize string handling with `strings.Builder`? Why can't you concatenate in a loop?</summary>

#### Go

Strings are immutable in Go. This means that each concatenation operation
creates a new string. Therefore, repeated `s += part` in a loop often generates
an avalanche of allocations and copies.

#### Why concatenation in a loop is inefficient:

1. A new row is created on each iteration.

2. Old content is copied over and over again.

3. Total cost can grow quadratically for large volumes.

4. Increasing pressure on the GC due to short-lived intermediate objects.

#### How `strings.Builder` helps:

1. `Builder` accumulates data in an internal buffer.

2. Entries (`WriteString`, `WriteByte`, `WriteRune`) minimize redundant copies.

3. The final line is generated once through `String()`.

4. Can be called `Grow(n)` if needed to pre-reserve capacity and reduce
   reallocation.

#### Practical advantages:

1. Less allocations.

2. Better throughput in formatting/text generation hot paths.

3. More stable latency behavior under load.

#### When it is especially necessary to use:

1. Generation of large payloads (JSON/SQL/HTML/log lines).

2. String construction in loops.

3. Any operations where a string is formed from many fragments.

#### Conclusion:

Concatenation in a loop is expensive due to repeated allocations and copying of
immutable rows. `strings.Builder` is an idiomatic and efficient tool for
constructing strings in Go, especially in performance-sensitive places.

#### Example:

```go
var b strings.Builder
b.Grow(1024)

for _, part := range parts {
	b.WriteString(part)
}

result := b.String()
```

</details>


<details>
<summary>70. How to optimize serialization?</summary>

#### Go

Optimizing serialization in Go is primarily work with allocations, data format,
buffer reuse, and reducing reflection in hot paths. Only a profiled approach
gives the best result, not "blind" micro-optimizations.

#### Practical optimization strategies:

1. **Selecting a format for the task:**

- JSON is convenient and versatile, but heavier than CPU;

- Protobuf/MessagePack are often faster and more compact for inter-service
  traffic.

2. **Reduction of allocations:**

- reuse `bytes.Buffer` / `[]byte` via `sync.Pool`;

- avoid unnecessary intermediate objects during marshal/unmarshal.

3. **Thread Serialization:**

- use `Encoder/Decoder` for large streams to avoid keeping the entire payload in
  memory at once.

4. **Data structure optimization:**

- remove unnecessary fields;

- use correct tags (`omitempty`, short keys if necessary);

- avoid overly nested structures unless required by business logic.

5. **Avoidance of redundant reflection in hot-path:**

- in critical places consider code generation or manual optimized
  (de)serialization.

6. **Payload size control:**

- compression is appropriate only after measurements, because it adds CPU costs;

- sometimes it is better to transmit less data than to compress "better".

#### How to evaluate the effect:

1. Benchmarks (`go test -bench`) before/after.

2. CPU/alloc profiles (`pprof`).

3. Production metrics: throughput, p95/p99 latency, heap, GC.

#### Conclusion:

Optimal serialization is a balance of format, allocations, and code complexity.
In Go, it's best practice to profile, clean up redundant copies, reuse buffers,
and choose a format that meets the requirements of a particular system.

</details>


<details>
<summary>71. How to optimize work with files?</summary>

#### Go

Optimizing file I/O in Go is about choosing the right read/write pattern, buffer
size, concurrency level, and disk strategy. The main goal is to reduce system
calls, redundant copies and deadlocks.

#### Key practices:

1. **Buffered I/O (`bufio.Reader/Writer`):** reduces the number of small
   `read/write` and increases throughput.

2. **Batch processing instead of byte-by-byte access:** reading/writing in
   blocks is much more efficient than small operations.

3. **Threading of large files:** do not load the entire file into memory if it
   can be processed in parts.

4. **Proper handle management:** `defer file.Close()` immediately after opening;
   this is basic hygiene to avoid FD leaks.

5. **Concurrency control:** parallelism is only useful within disk/FS bandwidth;
   excessive parallel I/O operations can degrade latency.

6. **Minimize redundant copies:** use `io.Copy` and reuse buffers where
   appropriate.

7. **Pre-Optimization Profiling:** measure whether the bottleneck is in disk,
   CPU, serialization or synchronization.

#### Additional engineering tips:

1. For logs/events, consider the flush policy (frequent flushes = lower
   throughput).

2. For large pipelines, separate reading, processing, and writing into
   manageable stages.

3. For critical scenarios, check file system and container/host settings (I/O
   quota, volume type, network storage).

#### Conclusion:

Working efficiently with files in Go is a discipline of buffering, streaming,
controlled parallelism, and measurements. Optimization should be based on the
real load profile, not on general assumptions.

</details>


<details>
<summary>72. How does batching work and when is it appropriate?</summary>

#### Go

`Batching` is the combination of many small operations into larger packages
(batch) to reduce the overhead of each individual operation. In highly loaded
systems, this is one of the most effective ways to increase throughput.

#### How batching works:

1. Events/records accumulate in the buffer.

2. Batch is sent according to one of the triggers:

- reached size `N`;

- timeout `T`;

- complete/flush received.

3. The operation is performed by one "batch" call (DB, network, disk, queue).

#### Why it is effective:

1. **Fewer system calls and round-trips.**

2. **Better loading of the I/O channel** (network, disk, database).

3. **Less synchronization overhead** for large numbers of small tasks.

#### When batching is appropriate:

1. Mass operations of the same type (logging, telemetry, bulk insert/update).

2. Scenarios where throughput is more important than the minimum possible unit
   latency.

3. Integrations where the external system works well with batch requests.

#### When batching can be harmful:

1. Strict requirements for the delay of a single operation.

2. Failed batch-size/timeout configuration, increasing tail latency.

3. High risk of losing a large block of data without proper retry/flush logic.

#### Practical rules:

1. Set **both size and time** (`N` + `T`) at the same time.

2. Have an explicit flush at shutdown.

3. Provide retry/backoff for partial or complete failures of batch requests.

4. Measure throughput ↔ latency balance on real load.

#### Conclusion:

Batching is an architectural performance multiplier for bulk operations. Its
power is revealed where the reduction of per-request overhead is more important
than the instantaneous response of each single event.

</details>


<details>
<summary>73. When is code generation (`go generate`) better than reflection?</summary>

#### Go

`Code generation` and `reflection` solve similar metaprogramming problems, but
have different prices. In Go, code generation often wins where speed, type
safety, and predictability are needed in production.

#### When `go generate` is better than reflection:

1. **Hot-path performance is critical:** generated code runs without runtime
   reflection, so it's usually faster and with smaller allocations.

2. **Strong type safety required:** errors are detected at compile time, not at
   runtime.

3. **High latency/throughput requirements:** serialization, mapping, RPC codecs,
   validation in bulk requests.

4. **Stable data contract:** when schemas are known in advance and rarely
   change.

5. **Requires transparent debugging:** generated calls can be profiled and
   analyzed like regular Go code.

#### When reflection is justified:

1. The scheme is dynamic and defined only at runtime.

2. Requires rapid prototyping or universal library flexibility.

3. Low performance requirements, where it is easier to accept the runtime
   overhead.

#### Compromises `go generate`:

1. Adds a step in build/workflow.

2. Must support templates/generators.

3. The generated code increases the size of the repository.

#### Practical conclusion:

If the system is performance sensitive and the default model is stable, `go
generate` is usually better than reflection. Reflection is appropriate where the
main value is dynamism, and not maximum performance efficiency.

</details>


<details>
<summary>74. What is Escape Analysis and how to check it with compiler flags?</summary>

#### Go

`Escape Analysis` is a Go compiler analysis that determines whether a value can
remain on the stack or must be allocated on the heap because it "runs away" from
the current stack frame.

#### Why is it important:

1. Stack allocations are cheaper.

2. Heap allocations increase GC pressure.

3. Understanding escape behavior helps optimize hot paths.

#### Typical reasons for escape:

1. Return pointer to local value.

2. Preserving value in a long-lived structure.

3. Capture of variable by closure.

4. Passing a value into contexts where the compiler cannot guarantee a local
   lifecycle.

#### How to check compiler flags:

The most used method:

1. `go build -gcflags="-m" ./...`

2. For more detailed output: `go build -gcflags="-m -m" ./...`

Messages are searched for phrases like:

- `moved to heap`

- `escapes to heap`

This is a direct indicator that no value has been left on the stack.

#### Practical process:

1. Run the benchmark/profile and find the hot fragment.

2. Check compiler escape output for this section.

3. Refactor locally (without degrading readability).

4. Remeasure effect (`bench`, `pprof`, allocs/op).

#### Conclusion:

Escape Analysis is a compiler "radar" for allocation behavior. `-gcflags="-m"`
allows you to see where data is leaking into the heap and make informed
decisions about memory and performance optimization.

</details>


<details>
<summary>75. Why are `panic` and `recover` not a replacement for normal error handling?</summary>

#### Go

In Go, `panic/recover` are for exceptional, emergency situations, not for normal
business logic error handling. The normal way to handle errors is to explicitly
return `error` and control the execution flow.

#### Why `panic/recover` is not replaced by `error handling`:

1. **Violate contract clarity:** with `error`, the function signature explicitly
   shows what can go wrong; with `panic` the error becomes implicit.

2. **Make flow control more difficult:** panic unwinds the stack, making the
   behavior less predictable for the caller.

3. **Test worse:** testing for panic scenarios is more difficult and less
   natural than testing for returned errors.

4. **Deteriorate the reliability of services:** an uncaught panic in a goroutine
   can destroy a process or an important processing loop.

5. **`recover` is local in nature:** works only in `defer` the same goroutine,
   so it is not a universal error mechanism between components.

#### When `panic` is justified:

1. Violation of internal invariants, which means a software error.

2. Contractually impossible states ("this should never happen").

3. Critical initialization failures when continuing is incorrect.

#### When `error` is needed:

1. Expected failures of external systems (network, DB, I/O).

2. Validation and domain errors.

3. Any situations where the caller has a choice of how to respond.

#### Conclusion:

In mature Go code, `error` is the primary tool for managed error handling.
`panic/recover` is an emergency mechanism for exceptional cases, not an everyday
alternative to standard error handling.

</details>


<details>
<summary>76. How do `errors.Is` and `errors.As` work with error wrapping in Go and what is the difference between them?</summary>

#### Go

In modern Go, errors are often "wrapped" by adding context via `fmt.Errorf("...:
%w", err)`. `errors.Is` and `errors.As` allow you to work correctly with such a
chain of errors without losing the original cause.

#### How `errors.Is` works:

1. Checks if the error chain contains a specific target error.

2. Used mainly for sentinel errors (`io.EOF`, `context.Canceled`, etc.).

3. Semantics: **"is this (or a wrapped version) the exact error?"**

#### How `errors.As` works:

1. Searches the chain for an error of a specific type.

2. If found, writes it to the passed target (pointer).

3. Semantics: **"can an error of this type be removed from the string?"**

#### Key Difference:

1. `errors.Is` — error **identity/equivalence** check.

2. `errors.As` — **type** checking and access to type-specific fields/methods.

#### Practical pattern of use:

1. First `errors.Is` for known sentinel cases.

2. Then `errors.As` if custom-type details (code, metadata, context) are
   required.

3. Do not compare wrapped errors through `==`, because this way correctness is
   lost in the wrapping chain.

#### Conclusion:

`errors.Is` answers the question "is this the same error?", and `errors.As`
answers "is this the same type of error?". Together, they form a correct and
reliable model for working with error wrapping in Go.

#### Example:

```go
if err := repo.Save(ctx, x); err != nil {
	return fmt.Errorf("save user: %w", err)
}

if errors.Is(err, sql.ErrNoRows) {
	// перевірка sentinel-помилки
}

var ve *ValidationError
if errors.As(err, &ve) {
	// доступ до полів конкретного типу помилки
}
```

</details>


<details>
<summary>77. When should you use custom error type instead of sentinel error and what are the practical consequences of this choice for the architecture?</summary>

#### Go

`Sentinel error` and `custom error type` are different error modeling tools.
Sentinel is suitable for a simple binary signal, and custom type - when the
error carries a structured context and affects the behavior of several layers of
the system.

#### When sentinel error is enough:

1. Only the fact of the specific error category is required.

2. No need to pass additional fields.

3. Checking through `errors.Is` is sufficient.

#### When is a custom error type:

1. Requires **structured details**:

- error code;

- domain reason;

- resource identifier;

- retryability;

- HTTP/gRPC mapping.

2. Different layers must make different decisions based on these fields.

3. Require stable evolution of error contract without chaotic string checks.

#### Architectural consequences of the choice:

1. **Sentinel error**

- an easier start;

- less code;

- but weaker expressiveness and risk of "growth" of implicit processing rules.

2. **Custom error type**

- clearer domain contract;

- better integration between transport/service/domain layers;

- higher testing of processing policies;

- but requires design discipline and a versioning approach.

#### Recommended practice:

1. For simple global signals — sentinel.

2. For domain-significant errors — custom type + `errors.As`.

3. Wrap lower errors through `%w` without losing causation.

#### Conclusion:

The choice between sentinel and custom type is a choice of the expressiveness
level of the error architecture. When an error affects decision routing in the
system, a custom error type provides a much more robust and scalable contract.

</details>


<details>
<summary>78. How does `defer` behave inside a loop and what might be the memory and performance implications?</summary>

#### Go

`defer` in Go is not executed at the end of the loop iteration, but at the
moment of exit from the surrounding function. Therefore, `defer` inside the loop
accumulates and is triggered only after the completion of the entire function.

#### How it works:

1. Each iteration adds a new deferred call to the defer stack.

2. These calls are not executed until the end of the function.

3. They are run in reverse (LIFO) order on exit.

#### Potential consequences:

1. **Delayed release of resources:** files, sockets, transactions, locks may
   remain open longer than necessary.

2. **Increased memory consumption:** many defer entries in a long loop increase
   overhead.

3. **Performance degradation:** in hot loops, excessive defers add
   runtime-overhead.

4. **Risk of running out of resources:** eg "too many open files" if `defer
   file.Close()` is in a long read cycle.

#### When it's safe:

1. Small number of iterations.

2. Short function life cycle.

3. Resources are not scarce.

#### Best practice for loops:

1. Put the iteration body into a separate function and put `defer` there.

2. Or close/release the resource explicitly at the end of each iteration.

3. For locks, it is especially important to control the holding time of the
   critical section.

#### Conclusion:

`defer` in a loop is a tool that requires discipline: it simplifies code, but
can stealthily accumulate resources and overhead. If there are many iterations,
it is better to ensure that resources are released within each step.

</details>


<details>
<summary>79. How does the `init` function work and can you rely on the order of its execution?</summary>

#### Go

`init` in Go is a special package function that is executed automatically during
program initialization (before `main`). It is used for initial setup, which
should happen once before starting the main logic.

#### How initialization works:

1. Imported dependencies are initialized first.

2. The package variables are then initialized.

3. After that, the `init` functions of the package are called.

4. Only after the entire initialization tree has completed does `main` run.

#### Can you rely on the order:

1. **Between packages**: yes, within dependencies, the order is defined - first
   dependencies, then consumer package.

2. **Within one package**:

- the order of initialization of variables is determined by dependencies between
  them;

- for multiple `init` different files in the same package, relying on a "random"
  text file order is a bad design idea.

3. Conclusion: there are basic guarantees, but architecturally it is better not
   to build critical business logic on complex implicit `init` chains.

#### Risks of overuse `init`:

1. Implicit side effects.

2. Heavier debugging and testing.

3. More complex order control in large codebases.

#### Practical recommendation:

1. Keep `init` minimal and predictable.

2. Use explicit constructors/`Setup`-functions for important initializations.

3. Dependencies and launch order should be fixed explicitly in the composition
   layer.

#### Conclusion:

`init` in Go is performed automatically and has formal order guarantees at the
level of the import graph. However, for a readable, testable architecture, it is
better to make critical initializations explicit rather than relying on hidden
`init` effects.

</details>


<details>
<summary>80. Why should you avoid global variables and `init` functions in libraries?</summary>

#### Go

In library code, global variables and "heavy" `init` functions often create
implicit behavior that makes it difficult to integrate, test, and predict the
application. This is especially critical for reusable packages.

#### Why global variables are bad in libraries:

1. **Hidden shared mutable state:** A consumer of the library may not know that
   there is global state somewhere that affects behavior.

2. **Competitiveness issues:** globals easily become a source of
   race/contention.

3. **Complex testing:** tests start to depend on the run order and side effects
   of previous cases.

4. **Poor composability:** it is difficult to have multiple independent library
   instances with different settings.

#### Why "heavy" `init` is undesirable:

1. **Implicit import side effects:** just `import` and the code is already
   executed.

2. **No explicit initialization time control:** It is difficult to control the
   startup order/conditions in a large application.

3. **Degraded observability/debuggability:** startup errors and side effects are
   harder to localize.

#### What is better instead:

1. Explicit constructors (`New(...)`) and configuration structures.

2. Instance-oriented design without global mutable state.

3. Explicit `Setup/Start/Close` lifecycle where needed.

4. Minimum `init` only for actions without side effects.

#### Conclusion:

The library should be predictable and user-driven. Avoiding global state and
excessive `init` is an investment in the testability, scalability, and
architectural purity of Go code.

</details>


<details>
<summary>81. What happens if you serialize to JSON a structure with fields starting with a lowercase letter?</summary>

#### Go

In Go, struct fields starting with a lowercase letter are non-exportable
(`unexported`). The `encoding/json` package does not have reflective access to
them as public fields, so they are ignored during serialization.

#### What happens with `json.Marshal`:

1. Only exported fields (in upper case) will be included in JSON.

2. Lowercase fields will be ignored.

3. The `json:"..."` tags on non-exported fields do not "force" them to be
   serialized.

#### Consequences in practice:

1. Unexpectedly "empty" or incomplete JSON.

2. Loss of important data in API responses.

3. Difficult to debug errors if the developer didn't take the export rule into
   account.

#### What about deserialization (`json.Unmarshal`):

1. Similarly, `encoding/json` will not write data to non-exported fields
   directly.

2. Process control requires custom `MarshalJSON` / `UnmarshalJSON` , separate
   DTOs, or other explicit transformation mechanisms.

#### Rule of thumb:

1. For fields to be JSON, use exported names.

2. Keep domain-sensitive internal data unexported deliberately.

3. Separate internal models and transport DTOs when fine-grained public contract
   control is required.

#### Conclusion:

In Go, JSON serialization only works with exported structure fields. Lowercase
fields in standard `encoding/json` are not serialized, even if they are tagged.

</details>


<details>
<summary>82. What are some ways to get data from JSON in Go?</summary>

#### Go

There is no single "right" way to work with JSON in Go: the approach is chosen
based on schema stability, performance requirements, and level of type safety.

#### Main methods:

1. **Decoding to structure (`struct`)**

- the most typical and most reliable option for a known scheme;

- provides type safety, clear contracts, and better maintainability.

2. **Decoding in `map[string]any`**

- is convenient for partially dynamic payloads;

- flexible, but less secure: requires assertions and type checks.

3. **Stream reading via `json.Decoder`**

- is suitable for large JSON or streams (HTTP body, files);

- allows you to work without loading the entire document into memory.

4. **`json.RawMessage` for deferred/partial parsing**

- useful when part of the scheme depends on the "discriminator" field;

- gives control over the decoding steps.

5. **Custom `UnmarshalJSON` / `MarshalJSON`**

- for non-standard formats, validation or special business semantics.

6. **Third libraries / codegen**

- is appropriate for high-performance or specific compatibility requirements.

#### Practical choice:

1. Stable API contract → `struct`.

2. Dynamic or partially unknown JSON → `map` + `RawMessage`.

3. Large volumes of data → `Decoder` (streaming).

4. Critical performance/pathological JSON → profiling + codegen/alternatives.

#### Conclusion:

The optimal way to "fetch" JSON data in Go depends on the nature of the schema.
In most production cases, typed structures are the basic choice, and dynamic
mechanisms (`map`, `RawMessage`, custom unmarshal) — for more complex scenarios.

</details>


<details>
<summary>83. What is the difference between `json.Marshal` and `json.Encoder`?</summary>

#### Go

`json.Marshal` and `json.Encoder` perform a similar serialization task, but have
a different memory and I/O model. The choice depends on whether you want a
ready-made `[]byte` or streaming directly to `io.Writer`.

#### `json.Marshal`:

1. Returns serialized JSON as `[]byte`.

2. Convenient when you need:

- get a byte array for further processing;

- log/sign/compress payload before sending;

- work with JSON in memory.

3. Minus: for large objects, it may require more memory, because the result is
   first completely formed in the buffer.

#### `json.Encoder`:

1. Writes JSON immediately to `io.Writer` (`http.ResponseWriter`, file, socket).

2. Suitable for streaming script and large responses.

3. Often more convenient in HTTP handlers, because it reduces intermediate
   buffers.

4. `Encode` adds a newline character at the end (this is important to note).

#### Practical rule of choice:

1. Require JSON as value in code → `json.Marshal`.

2. Must write to stream/response → `json.NewEncoder(w).Encode(...)` immediately.

#### Conclusion:

`Marshal` — "form JSON in memory", `Encoder` — "write JSON to stream".
Functionally, they are close, but from the point of view of resources and I/O
architecture, the difference is fundamental.

#### Example:

```go
// Marshal: отримуємо JSON у []byte
payload, err := json.Marshal(resp)
if err != nil { return err }
_ = payload

// Encoder: пишемо JSON одразу у HTTP-відповідь
w.Header().Set("Content-Type", "application/json")
if err := json.NewEncoder(w).Encode(resp); err != nil {
	return err
}
```

</details>


<details>
<summary>84. What is `json.RawMessage` and when is it useful?</summary>

#### Go

`json.RawMessage` is a type (essentially `[]byte`) from the `encoding/json`
package that allows you to save a JSON fragment "as is" without immediately
parsing it into a specific structure.

#### What it does:

1. **Deferred Parsing:** only the "wrapper" of the message can be parsed first,
   and the complex field later when the required type is known.

2. **Partial decoding:** we analyze only those parts of the payload that are
   really needed in this step.

3. **Transparent Retransmission:** A JSON fragment can be retransmitted without
   losing the original representation.

#### When it is especially useful:

1. **Polymorphic payloads:** when the field type depends on the
   `type/kind/version`-discriminator.

2. **Event-driven systems:** the event wrapper is stable and the event body has
   different schemas.

3. **Integration gateways:** need to read the routing metadata and pass the
   "body" on almost unchanged.

4. **Performance optimization:** avoiding unnecessary full unmarshal for large
   or partially unnecessary objects.

#### What to consider:

1. `RawMessage` does not automatically validate the semantics — the validation
   is left to your logic when `Unmarshal` follows.

2. Deferred parsing complicates code if applied unnecessarily.

#### Conclusion:

`json.RawMessage` is a tool for managed "late binding" of JSON data. It is
especially valuable in polymorphic and multi-format protocols, where the type of
the internal payload is determined only at runtime.

</details>


<details>
<summary>85. How to implement a custom marshaler for JSON?</summary>

#### Go

A custom marshaler in Go is implemented through the `MarshalJSON() ([]byte,
error)` method on your type. This allows full control over how an object is
serialized into JSON: field format, validation, computed values, masking, etc.

#### Basic approach:

1. Add method: `func (t MyType) MarshalJSON() ([]byte, error)`.

2. Internally create an intermediate representation (often an alias/DTO
   structure).

3. Call `json.Marshal` for this view.

4. Return bytes or error.

#### Why do they do it:

1. **Non-standard output format:** eg time conversion, enum, decimal, mask
   fields.

2. **External contract compatibility:** when an API requires a specific schema
   or naming convention.

3. **Managed data hiding:** do not output sensitive fields or generate a
   redacted version.

4. **Computed/derived fields:** include values ​​in JSON that are not present as
   "raw" structure fields.

#### A typical technique without recursion:

To avoid an infinite call to `MarshalJSON`, use the alias type (`type alias
MyType`) and marshal the alias or a separate DTO.

#### Important tips:

1. Keep marshalling logic deterministic and simple.

2. Write tests on edge-cases and backward compatibility of the JSON contract.

3. If symmetry is required, also implement `UnmarshalJSON`.

#### Conclusion:

Custom `MarshalJSON` is a tool for fine-tuning public exposure. In production,
it is used when standard tags are not sufficient for contract, security or
domain semantics.

</details>


<details>
<summary>86. How to parse multi-typed JSON if the input data or any of the fields can be either a `[...]` array or a `{...}` object?</summary>

#### Go

When a JSON field has a "float" form (sometimes an array, sometimes an object),
the most reliable approach in Go is deferred decoding via `json.RawMessage` or
custom `UnmarshalJSON` with actual type recognition.

#### Canonical strategy:

1. Decode the problematic field in `json.RawMessage`.

2. Look at the first significant byte:

- `[` → this is an array;

- `{` → this is an object.

3. Depending on the form, commit `json.Unmarshal` to the appropriate target
   type.

4. Normalize the result into an internal single model (so that the code does not
   depend on the external "fluid" scheme).

#### Alternative: Custom `UnmarshalJSON`:

1. Implement a method on your own type.

2. Inside the method, try parsing in `[]T`, and if it doesn't fit - in `T` (or
   vice versa).

3. Save in unified representation, eg always as `[]T`.

#### Why this is important:

1. External APIs are often inconsistent between versions/endpoints.

2. Direct `Unmarshal` into a hard structure gives errors like `cannot unmarshal
   object into Go value of type []...`.

3. Input normalization dramatically simplifies the rest of the business logic.

#### Practical tips:

1. Clearly document acceptable forms of input JSON.

2. Log anomalous payloads to diagnose contract failures.

3. Cover with tests both forms (`{}` and `[]`) + edge-cases (null, empty values,
   incorrect type).

#### Conclusion:

For multi-type JSON, the pattern "RawMessage → shape detection → target
Unmarshal → normalization" works best in Go. This gives stable processing even
with an unstable external contract.

</details>


<details>
<summary>87. How to test serialization (XML/JSON) in Go when the order of the keys in the map is not deterministic?</summary>

#### Go

When the order of keys in `map` is non-deterministic, tests cannot be built on a
literal comparison of "raw" serialization strings. The correct approach is to
compare the content, not the random order of presentation.

#### Robust strategies for JSON:

1. **Round-trip structure comparison:**

- serialize;

- deserialize back to type/normalized model;

- compare data as a structure.

2. **Canonicalization before comparison:**

- parse JSON into intermediate model;

- sort keys/collections;

- compare canonical view.

3. **Semantic assertions instead of string equality:**

- check specific fields and invariants.

#### For XML:

1. Similar principle: compare element/attribute tree, not raw string.

2. Normalize spaces, formatting, order of attributes (if the contract allows
   it).

3. Check the semantic equivalence of parsed structures.

#### When you need a golden file:

1. Form **deterministic output**:

- sort keys before serialization;

- or serialize not `map` but a struct/ordered list of pairs.

2. Golden test should fail only on semantic changes of the contract, not random
   order of keys.

#### Practical conclusion:

Serialization tests for `map` do not compare "text one-to-one", but data
equivalence. Determinism must either be introduced explicitly (sorting), or
apply semantic-level checks.

</details>


<details>
<summary>88. What are the advantages and disadvantages of Protobuf compared to JSON? How is serialization different in Protobuf?</summary>

#### Go

Protobuf and JSON are two different classes of formats: JSON is focused on human
readability and versatility, while Protobuf is focused on compactness, speed,
and machine interaction contractibility.

#### Advantages of Protobuf over JSON:

1. **More compact payload size:** binary encoding is usually significantly
   smaller than textual JSON.

2. **Higher serialization/deserialization performance:** less parsing overhead
   and better throughput in interservice traffic.

3. **Strict schema-first contract (`.proto`):** Clear typical model, codegen and
   field evolution control.

4. **Better backward/forward compatibility by field and tag rule.**

#### Disadvantages of Protobuf:

1. **Less eye-readable:** binary format is not convenient for manual debugging
   without tools.

2. **Additional infrastructure:** `.proto`, code generation, schema versioning.

3. **Entry threshold is higher than JSON.**

#### Advantages of JSON:

1. Easy integration and quick start.

2. Human readability and convenience of manual analysis.

3. Broad compatibility in the web ecosystem.

#### How serialization differs in Protobuf:

1. Data is encoded not by field names, but by numeric tags (`field numbers`).

2. The format is binary, with distinct wire-level types.

3. Structures are generated from `.proto` (code generation), not reflected as in
   a typical JSON stream.

4. Contract evolution requires discipline:

- do not reuse old tags;

- carefully change the types/optional/repeated fields.

#### Conclusion:

JSON is better for open, human-centric APIs and fast integration. Protobuf is
for high-performance interservice systems with a clear schematic contract, where
payload size, latency and stability of evolution are critical.

</details>


<details>
<summary>89. Why should `http.Client` be reused instead of creating a new one for each request?</summary>

#### Go

In Go, `http.Client` and its transport (`http.Transport`) manage TCP connection
pooling, keep-alives, TLS sessions, and other network optimizations. If you
create a new client for each request, these benefits are lost.

#### Why reuse is important:

1. **Connection pooling:** reusing already open connections reduces latency.

2. **Less handshake overhead:** fewer TCP/TLS setups per request.

3. **Better throughput:** more stable throughput in high-load scenarios.

4. **Resource Control:** Mass creation of new clients/transports can increase
   the number of sockets and exhaust system resources.

#### What happens with "client per request":

1. Worse disposal of keep-alive.

2. More short-lived connections.

3. Higher latencies and extra network/CPU pressure.

#### Recommended practice:

1. Have a long-lived `http.Client` (often one per service or policy class).

2. Configure timeouts and parameters `Transport` explicitly under workload.

3. For different SLAs/Routes - Separate reuse clients, but not "new client per
   call".

#### Conclusion:

`http.Client` should be reused in Go because it provides network efficiency,
lower latency, and better stability under load. Creating a new client for each
request is a typical anti-practice for production systems.

</details>


<details>
<summary>90. Why must you close `resp.Body` after an HTTP request?</summary>

#### Go

`resp.Body` in Go is a streaming resource associated with a network connection.
If it is not closed, the client will not be able to correctly return the
connection to the pool or release system resources, which leads to service
degradation.

#### Why this is critical:

1. **Resource leak:** unclosed bodies hold handles and sockets.

2. **Deterioration of connection reuse:** keep-alive works worse, the number of
   new connections increases.

3. **Increasing latency and errors under load:** possible exhaustion of the
   connection pool and system limits.

4. **Unstable client behavior:** "hangs", timeouts, unexpected failures in
   high-frequency calls.

#### Correct pattern:

1. After checking the error from `Do` immediately do: `defer resp.Body.Close()`.

2. If you need maximum reuse connections:

- read body to the end (or correctly limit reading),

- and then close.

#### Practical conclusion:

The `resp.Body` closure is not a formality, but a prerequisite for the correct
operation of the HTTP client in Go. This directly affects the performance,
stability and resource efficiency of the service.

#### Example:

```go
resp, err := client.Do(req)
if err != nil {
	return err
}
defer resp.Body.Close()

body, err := io.ReadAll(resp.Body)
if err != nil {
	return err
}
_ = body
```

</details>


<details>
<summary>91. How is `http.DefaultServeMux` different from custom `ServeMux`?</summary>

#### Go

`http.DefaultServeMux` is the "default" global router. A custom `ServeMux` is a
separate explicitly created router instance that you manage locally within a
specific server.

#### `http.DefaultServeMux`:

1. **Global package state `net/http`:** registration via `http.Handle` /
   `http.HandleFunc` writes exactly there.

2. **Quickstart:** good for simple examples and small utilities.

3. **Risks in larger projects:** implicit registrations from different packages,
   more complex control of dependencies and tests.

#### Custom `ServeMux`:

1. **Explicit composition:** `mux := http.NewServeMux()` and passing it to
   `http.Server{Handler: mux}`.

2. **Route isolation:** each server/test/instance can have its own handler
   table.

3. **Better testability and maintainability:** fewer global side effects, easier
   to do independent integration tests.

4. **Safer architecture for monoliths and microservices:** routing becomes part
   of the explicit bootstrap code.

#### Practical choice:

1. For production code, custom `ServeMux` is almost always better.

2. `DefaultServeMux` is mostly appropriate for very simple scenarios or
   tutorials.

#### Conclusion:

The difference between them is in the level of transparency and control.
`DefaultServeMux` convenient but global; custom `ServeMux` gives isolated,
controlled, and architecturally cleaner routing.

</details>


<details>
<summary>92. How to properly implement graceful shutdown of HTTP server and background worker in Go?</summary>

#### Go

`Graceful shutdown` in Go is a controlled service termination without losing
requests and without "orphaned" goroutines. The idea is simple: stop receiving a
new load, let the active work finish, correctly stop the background and close
the resources in a predictable sequence.

#### Canonical sequence:

1. Intercept completion signals (`SIGTERM`, `SIGINT`).

2. Create `context` with timeout for shutdown phase.

3. Call `server.Shutdown(ctx)`:

- new connections are no longer accepted;

- active requests are given time to complete.

4. Cancel context/signal background workers to stop.

5. Wait for completion of workers (`WaitGroup`/`errgroup`).

6. Close external resources (DB, queues, producers, files).

#### How to stop a background worker:

1. Worker runs in a loop with `select` where there is a branch `case
   <-ctx.Done(): return`.

2. On shutdown, the main process calls the cancel function.

3. The worker completes the current protected step, does a flush/cleanup and
   exits.

#### Critical practices:

1. **Timeouts are required:** graceful should not turn into an eternal wait.

2. **Idempotent shutdown:** repeated signals do not break the shutdown logic.

3. **Observability:** log stop stages and duration metrics.

4. **Clear order:** first stop intake, then drain in-flight, then cleanup.

#### Typical errors:

1. Stop the process "hard" without `Shutdown`.

2. Do not pass `ctx` to workers/external calls.

3. Do not wait for goroutines to finish.

4. Forget about flush buffers/queues before exit.

#### Conclusion:

A proper graceful shutdown in Go is orchestrated via a signal, `context`,
`server.Shutdown` and explicitly waiting for all background tasks. This approach
guarantees the integrity of requests, predictable output and reliability of
operation.

</details>


<details>
<summary>93. Why compare `time.Time` over `.Equal()` and not `==`?</summary>

#### Go

In Go, `time.Time` should be compared over `t1.Equal(t2)` because `==` checks
the bit-to-bit structure of the value, including supporting internals (including
the location and, under certain conditions, the monotonic part of the time), not
just the point in time on the timeline.

#### Why `==` can give a false result:

1. Two `time.Time` can represent the same instance but have different location
   representations.

2. Internal service data may vary, although the calendar moment is the same.

3. So `t1 == t2` can be `false` even when the time point is equivalent.

#### What `.Equal()` does:

1. Compares exactly the temporal instant (moment semantics) and not the internal
   representation of the structure.

2. This is a valid "is it the same time?" business logic check.

#### When `==` is still appropriate:

1. To check for a null value: `t == (time.Time{})`.

2. For cases where you really need to compare full structural identity, not just
   an instant.

#### Practical conclusion:

In applied timing logic, use `.Equal()`. The `==` operator for `time.Time` is
easily error-prone because it compares more than is usually intended when
checking for moment equivalence.

</details>


<details>
<summary>94. How do indexes work? How to choose indexes for tables?</summary>

#### Go

An index in a DBMS is an auxiliary data structure (most often B-tree-like),
which speeds up the search for rows by certain fields without a full table scan.
In fact, an index stores an ordered representation of keys and references to
rows.

#### How indexes work:

1. A query with `WHERE/JOIN/ORDER BY` can use an index to quickly find a
   relevant range of keys.

2. Instead of `Seq Scan` (full table read), the optimizer chooses `Index
   Scan/Bitmap Scan` if it is beneficial.

3. Indexes can also support uniqueness (`UNIQUE`).

#### Index price:

1. Each index takes up disk space.

2. `INSERT/UPDATE/DELETE` become more expensive because you need to update the
   indexes.

3. Redundant indexes slow down writes and make maintenance difficult.

#### How to choose indexes correctly:

1. **Push off real requests**, not "just in case".

2. Index fields that are often in:

- `WHERE`

- `JOIN ON`

- `ORDER BY`

- `GROUP BY` (if needed)

3. For composite indexes, take into account the order of columns
   (leftmost-prefix rule):

- most selective/frequent conditions are at the beginning.

4. Watch `EXPLAIN (ANALYZE, BUFFERS)` and confirm that the index is actually
   used and profitable.

5. Review ineffective/unused indexes regularly.

#### Practical approach:

1. Define top slow requests.

2. Add minimum required indexes.

3. Check plan before/after.

4. Measure impact on read/write balance under real load.

#### Conclusion:

An index is a tool to speed up reading at the cost of writing more expensively.
The correct selection of indexes is always query-driven: only for specific
access patterns and only after plan and performance validation.

#### Example:

```sql
-- Перевіряємо план до індексу
EXPLAIN (ANALYZE, BUFFERS)
SELECT *
FROM orders
WHERE tenant_id = 42
  AND created_at >= now() - interval '7 days'
ORDER BY created_at DESC
LIMIT 100;

-- Додаємо індекс під реальний патерн запиту
CREATE INDEX CONCURRENTLY idx_orders_tenant_created_at
  ON orders (tenant_id, created_at DESC);
```

</details>


<details>
<summary>95. What is a Materialized View and how is it different from a regular View?</summary>

#### Go

`View` and `Materialized View` both represent a stored query, but differ
fundamentally in the way the result is stored and the cost of reading.

#### Normal `View`:

1. This is a logical "virtual table" based on an SQL query.

2. Data is not physically stored separately.

3. Each request to the view actually re-executes the underlying SQL.

#### `Materialized View`:

1. This is a physically stored query result.

2. Reading is usually much faster because you don't have to recalculate complex
   join/aggregate every time.

3. Data may be out of date by `REFRESH`.

#### Key Difference:

1. `View` = always up-to-date data, but higher calculation cost.

2. `Materialized View` = fast read, but compromise on data freshness.

#### When to choose `Materialized View`:

1. Heavy analytical queries and aggregations.

2. Frequently read reports with less frequent updates.

3. Scenarios where controlled relevance delay is acceptable.

#### When the usual `View` is enough:

1. The most up-to-date real-time data is required.

2. The request is not too expensive.

3. `View` is used as a logical access abstraction, not as a cache.

#### Practical conclusion:

`Materialized View` is essentially a managed SQL result cache with an explicit
update; plain `View` is a pure logical projection with no data storage. The
choice between them is a balance between freshness and speed.

#### Example:

```sql
CREATE MATERIALIZED VIEW mv_daily_sales AS
SELECT date_trunc('day', created_at) AS day,
       sum(amount) AS total
FROM payments
GROUP BY 1;

-- Оновлення знімка даних
REFRESH MATERIALIZED VIEW CONCURRENTLY mv_daily_sales;
```

</details>


<details>
<summary>96. What is ACID? Comment on how ACID is implemented in PostgreSQL.</summary>

#### Go

`ACID` are four basic properties of transactional systems that guarantee
correctness of data even under failures, competition and high load: Atomicity,
Consistency, Isolation, Durability.

#### ACID decryption:

1. **Atomicity:** a transaction is either fully executed or not executed at all.

2. **Consistency:** after the commit, the data remains valid against the defined
   rules and restrictions.

3. **Isolation:** parallel transactions should not improperly affect each other.

4. **Durability:** Committed changes persist even after a process/system
   failure.

#### How PostgreSQL implements ACID:

1. **Atomicity:**

- transaction log of changes + rollback mechanisms;

- in the event of an error, all transaction changes will be rolled back as a
  whole.

2. **Consistency:**

- constraints (`PRIMARY KEY`, `UNIQUE`, `CHECK`, `FOREIGN KEY`) and triggers;

- commit is possible only if invariants are not violated.

3. **Isolation:**

- MVCC (Multi-Version Concurrency Control): readers see consistent versions of
  lines without gross blocking of reads;

- support of isolation levels (`Read Committed`, `Repeatable Read`,
  `Serializable`) with different balance of performance and strictness.

4. **Durability:**

- WAL (Write-Ahead Logging): before the commit, changes are first recorded in
  the log;

- after a failure, recovery takes place according to WAL, which preserves the
  committed state.

#### Practical conclusion:

In PostgreSQL, ACID is not provided by "one button", but by a combination of
MVCC, WAL, transaction manager, locks and constraint mechanisms. This is what
makes PostgreSQL a reliable DBMS for critical transactional systems.

#### Example:

```sql
BEGIN;

UPDATE accounts
SET balance = balance - 100
WHERE id = 1;

UPDATE accounts
SET balance = balance + 100
WHERE id = 2;

COMMIT; -- або ROLLBACK при помилці
```

</details>


<details>
<summary>97. What is the difference between BASE and ACID?</summary>

#### Go

`ACID` and `BASE` are two different philosophies of consistency and reliability
in distributed/transactional systems. They reflect different architectural
priorities: strictness and instant consistency versus availability and
scalability.

#### ACID:

1. **Atomicity, Consistency, Isolation, Durability**.

2. Focused on strict transactional guarantees.

3. Benefit — predictable correctness of data after each commit.

4. Typically used in financial, accounting, critical consistent scenarios.

#### BASE:

1. **Basically Available, Soft state, Eventual consistency**.

2. Focused on high availability and horizontal scaling.

3. Allows temporary inconsistency between nodes.

4. Consistency is achieved "over time", not necessarily instantly.

#### Key Difference:

1. **ACID**: "better to wait but keep strict guarantees".

2. **BASE**: "best to respond quickly and be available, even if consistency is
   not instant."

#### Practical implications for architecture:

1. ACID simplifies reasoning about invariants, but may cost more in terms of
   latency/scaling in a distributed environment.

2. BASE provides stability and availability at large scales, but requires
   compensation mechanisms, idempotency, and thoughtful domain design.

#### Conclusion:

ACID and BASE are not "good/bad" but different compromises. The choice depends
on what is more critical for the system: immediate stringency of invariants or
availability and scalability at the price of eventual consistency.

</details>


<details>
<summary>98. Name the transaction isolation levels.</summary>

#### Go

Isolation levels determine how "visible" the changes of parallel transactions
are to each other. The higher the level of isolation, the fewer anomalies, but
usually at a higher cost in performance and competitiveness.

#### Classic isolation levels (SQL):

1. **Read Uncommitted**

- lowest level;

- allows reading unfixed changes (dirty read).

2. **Read Committed**

- only committed data is read;

- dirty read is prohibited;

- non-repeatable read and phantom read are possible.

3. **Repeatable Read**

- reading the same lines repeatedly within a transaction gives the same result;

- reduces some of the anomalies, but depending on the DBMS, phantom scenarios
  may remain.

4. **Serializable**

- the strictest level;

- guarantees a result equivalent to sequential execution of transactions;

- maximum protection against anomalies, but more expensive than the competition.

#### Practical conclusion:

The choice of isolation level is a balance between correctness and performance.
In production, it is determined from domain invariants: where `Read Committed`
is sufficient, and where `Repeatable Read` or `Serializable` is required.

#### Example:

```sql
BEGIN;
SET TRANSACTION ISOLATION LEVEL REPEATABLE READ;

SELECT balance FROM accounts WHERE id = 1;
-- ... інші операції в межах тієї ж транзакції

COMMIT;
```

</details>


<details>
<summary>99. What are graph databases for?</summary>

#### Go

Graph databases are needed where the main value is not individual records, but
the connections between them and fast bypass of multi-step relationships.

#### What a graph database models:

1. **Nodes** are entities.

2. **Edges** — relationships between entities.

3. **Properties** of nodes and edges are attributes of the domain model.

#### For what tasks are they especially useful:

1. **Social graphs:** friends, subscriptions, recommendations.

2. **Fraud detection:** non-trivial chains of transactions and suspicious
   connections.

3. **Knowledge graph / semantic search:** connected representation of knowledge.

4. **Network/IT topology:** service dependencies, routes, impact of incidents.

5. **Role/permission models:** complex access policies with role inheritance.

#### Why a relational database is not always enough:

1. In multi-step join scenarios, queries can become heavy and cumbersome.

2. The graph engine is optimized specifically for traversal-path requests.

3. The "relationship as a first-class entity" model makes complex relationship
   cases more natural.

#### When a graph database is optional:

1. If connections are simple and are rarely queried deeply.

2. If classic CRUD/OLTP scenarios without complex traversal dominate.

3. If the team and infrastructure are already working effectively with the
   relational stack.

#### Conclusion:

Graph databases are needed when the business value lies in the structure of
connections and multi-step navigation through them. It is a specialized tool for
relationship-centric domains where a join-oriented approach becomes ineffective
or too complex.

</details>


<details>
<summary>100. If data is time-bound, which databases should I use?</summary>

#### Go

If the data has a specific time nature (metrics, logs, events, telemetry), it is
advisable to choose a DBMS according to the load profile: recording frequency,
type of requests, storage period, requirements for aggregations and latency.

#### Typical options:

1. **Time-series DB (TSDB)**

- examples: Prometheus (for metrics), VictoriaMetrics, InfluxDB, TimescaleDB;

- strengths: high speed of ingestion, requests for time windows,
  downsampling/retention policies.

2. **PostgreSQL + time-oriented approach**

- when you need transactionality, the SQL ecosystem, and complex join queries
  with time data;

- is often combined with time partitioning.

3. **Columnar OLAP storage**

- for analytics of large volumes of historical events (ClickHouse, etc.);

- strong in aggregates and scanning large time ranges.

#### Selection criteria:

1. **Write-heavy telemetry** → TSDB.

2. **Operational transactions + time** → PostgreSQL (with partitioning/indexes).

3. **Large-scale historical analytics** → columnar/OLAP approach.

4. **Retention and cost model**: hot data in the fast layer, cold data in the
   cheaper storage.

#### Practical conclusion:

There is no "universal" database for time-bound data: a combination of tools for
a specific workload is optimal. In most systems, a hot TSDB/OLTP layer strategy
combined with a separate analytical layer for long history works.

</details>


<details>
<summary>101. How does master-slave replication work?</summary>

#### Go

Master-slave (primary-replica) replication is a model in which one node accepts
writes and one or more replica nodes replicate those changes for read scaling,
redundancy, and increased fault tolerance.

#### Basic principle:

1. **Master (primary)** handles `INSERT/UPDATE/DELETE`.

2. Changes are recorded in the transaction log (WAL/binlog depending on the
   DBMS).

3. **Slave (replica)** reads the log and applies the changes to its copy of the
   data.

4. Reads are often distributed to replicas, writes are left on the primary.

#### Replication modes:

1. **Asynchronous**

- primary does not wait for confirmation from replica before committing;

- lower recording latency;

- possible replication lag and temporal inconsistency.

2. **Synchronous/quasi-synchronous**

- primary partially or fully waits for confirmation of replicas;

- higher consistency;

- potentially higher write latency.

#### What it does:

1. Scaling read load.

2. Backup copies of data for failover.

3. Separation of OLTP records and heavy-read scenarios.

#### Typical risks:

1. **Replication lag** (reader can see "old" data).

2. Complexity of failover/failback and node roles.

3. Risk of split-brain in incorrectly organized switching scenarios.

#### Practical conclusion:

Master-slave replication is a balance between availability, scalability, and
consistency. It is effective for read-scaling, but requires the discipline of
lag monitoring, thoughtful failover, and a clear request routing policy.

</details>


<details>
<summary>102. What is sharding and what are its types?</summary>

#### Go

Sharding is the horizontal division of data into several independent nodes
(shards) to scale the system beyond a single server in terms of data volume,
load, and bandwidth.

#### Why is sharding used:

1. Unrestrict single node (CPU/RAM/disk/I/O).

2. Increase write/read throughput through parallel operation of shards.

3. Localize hot datasets and reduce competition for resources.

#### The main types of sharding:

1. **Range-based sharding**

- data is partitioned by key ranges (for example, by date or ID interval);

- simple for time-series scenarios;

- risk of "hot" ranges.

2. **Hash-based sharding**

- shard is determined by the hash of the key;

- distributes the load more evenly;

- it is more difficult to make range queries.

3. **Directory / Lookup-based sharding**

- a separate table/service maps key → shard;

- flexible routing and migrations;

- additional complexity and dependency on the lookup layer.

4. **Geo / Tenant-based sharding**

- data is shared by region or client (tenant);

- good for isolation, compliance and multi-tenant architectures;

- possible imbalance between shards.

#### Architectural challenges of sharding:

1. Data rebalancing during growth.

2. Cross-shard requests, joins and transactions.

3. Complications of backup/restore and failover.

4. Increased complexity of observability and operational support.

#### Conclusion:

Sharding is a scaling tool that provides significant performance gains, but at
the cost of architectural complexity. The choice of sharding type should be
based on the data access pattern, domain model and system evolution plan.

#### Example:

```go
func shardForUser(userID int64, shards int) int {
	if shards <= 0 {
		return 0
	}
	return int(userID % int64(shards)) // hash/range-логіку змінюють під домен
}
```

</details>


<details>
<summary>103. Tell us about your experience with database optimization. What tools did you use?</summary>

#### Go

For an interview, this question usually expects a **structured case story**:
context → problem → actions → tools → before/after metrics. Below is a sample
strong response that you can adapt to your own real-world experience.

#### Example:

1. **Context**

- in a service with a high read/write load, degradation of p95/p99 latency was
  observed during peak hours.

2. **Symptoms**

- slow requests;

- CPU growth on the DB node;

- increasing lock wait and request queues.

3. **What did you do**

- collected the top slow requests;

- have analyzed execution plans;

- added/rebuilt indexes to real `WHERE/JOIN/ORDER BY`;

- removed N+1 and transferred some heavy operations to batch;

- added caching for hot read-cases;

- optimized the scheme (types of fields, partitioning by time, archiving of old
  data).

4. **Tools**

- `EXPLAIN (ANALYZE, BUFFERS)` / `EXPLAIN ANALYZE`;

- request statistics (`pg_stat_statements` or similar);

- application profiling (`pprof`) to separate the DB-bottleneck from the
  app-layer;

- metrics and dashboards (Prometheus/Grafana);

- load tests before/after changes.

5. **Result (formulation example)**

- p95 was conditionally reduced by 40–60%;

- throughput increased without additional DB nodes;

- stabilized peak periods and reduced lock-contention.

#### How to respond most convincingly:

1. Speak the language of measurements, not general phrases.

2. Explain the trade-off: what was accelerated and at what cost.

3. Emphasize a reproducible process: "first measured, then changed, then
   tested".

#### Conclusion:

A strong DB optimization answer is a proof-of-concept engineering case with
metrics and tools. It is this structure that demonstrates maturity and practical
competence.

</details>


<details>
<summary>104. How does `pgx` differ from `lib/pq` in terms of performance and functionality?</summary>

#### Go

`lib/pq` and `pgx` both work with PostgreSQL, but belong to different
generations of the Go ecosystem. In modern production scenarios, `pgx` is
generally considered a more practical choice.

#### Main difference:

1. **`lib/pq`**

- classic driver for `database/sql`;

- stable, but functionally conservative;

- fewer modern optimizations and PostgreSQL-specific features.

2. **`pgx`**

- modern driver/tools for PostgreSQL;

- can work both as a native API and through the `database/sql`-compatible layer;

- richer feature set and often better performance under real load.

#### Productivity:

1. `pgx` often shows better throughput and lower latency, especially in
   high-load scenarios.

2. Reasons: more efficient handling of the PostgreSQL protocol, better
   batching/copying capabilities, more flexible handling of types.

3. The final conclusion is always benchmarked against your workload.

#### Functionality:

1. `pgx` provides wider access to PostgreSQL specifics:

- extended typical system;

- batch/Copy-primitives;

- finer control of connection and query behavior.

2. `lib/pq` mostly remains a "barely sufficient" driver for basic tasks due to
   `database/sql`.

#### When to choose:

1. **`pgx`** — for new projects, high workload, need for modern PostgreSQL
   features and better control.

2. **`lib/pq`** — mostly legacy code, where migration is not yet justified.

#### Conclusion:

`pgx` usually wins in both functionality and performance potential. `lib/pq` is
historically important, but for most new Go/PostgreSQL systems, `pgx` is the
preferred choice.

</details>


<details>
<summary>105. How to write unit tests in Go?</summary>

#### Go

A unit test in Go tests a small, isolated unit of behavior (function/method)
with a clear input and expected result. The strength of the approach lies in
determinism, speed and transparency of the reasons for the fall.

#### Basic principles of a quality unit test:

1. **One behavior is one test intent.**

2. **Isolation from external systems** (DB, network, time, file system).

3. **Determinism**: The same conditions must produce the same result.

4. **Readability and diagnosticity** of error messages.

#### Idiomatic structure in Go:

1. File `*_test.go`.

2. View functions `func TestXxx(t *testing.T)`.

3. Arrange → Act → Assert pattern.

4. For multiple cases — table-driven tests.

#### What must be covered:

1. Positive scenarios (happy path).

2. Negative scripts and bugs.

3. Borderline cases (empty data, zeros, large values, incorrect input).

4. Invariants that must not be violated under any circumstances.

#### Practical tools:

1. Standard Package `testing`.

2. `go test ./...` for a regular run.

3. `-race` for competitive sites.

4. If necessary - `testify` (assert/require), but without excessive magic.

#### Typical errors:

1. Time/Network/Run Order dependent tests.

2. Checking only "without panic", without substantive assertions.

3. Too large integration scripts disguised as unit tests.

#### Conclusion:

Writing unit tests in Go means designing verifiable behavior: minimal volume, a
clear contract, isolation from the outside world, and reliable assertions. This
approach provides fast and stable regression protection.

#### Example:

```go
func TestSum(t *testing.T) {
	tests := []struct {
		name string
		a, b int
		want int
	}{
		{"pos", 2, 3, 5},
		{"zero", 0, 7, 7},
	}

	for _, tc := range tests {
		tc := tc
		t.Run(tc.name, func(t *testing.T) {
			got := Sum(tc.a, tc.b)
			if got != tc.want {
				t.Fatalf("got %d, want %d", got, tc.want)
			}
		})
	}
}
```

</details>


<details>
<summary>106. What is the difference between `t.Error` and `t.Fatal` in tests?</summary>

#### Go

`t.Error` and `t.Fatal` both mark the test as failing, but have different
behavior for continuing execution.

#### `t.Error`:

1. Logs an error and marks the test as failed.

2. **Does not stop** running the current test.

3. Suitable when we want to collect several independent checks in one run.

#### `t.Fatal`:

1. Logs an error and marks the test as failed.

2. **Immediately stops** the current test (`FailNow`).

3. Appropriate when, without this prerequisite, further checks do not make sense
   or may cause noise/panic.

#### Rule of thumb:

1. Use `t.Fatal` if the underlying premise is broken (eg failed to create test
   object, got `nil` where dereference follows).

2. Use `t.Error` if you want to check multiple independent postconditions and
   see all deviations at once.

#### Conclusion:

The difference is simple and fundamental: `t.Error` — "fix and continue",
`t.Fatal` — "fix and stop immediately". The choice depends on whether the test
remains meaningful after a particular error.

</details>


<details>
<summary>107. How does `testify/assert` differ from `testify/require` semantically?</summary>

#### Go

The semantic difference between `assert` and `require` is the same as between
`t.Error` and `t.Fatal` in standard `testing`: one allows the test to continue,
the other stops it immediately.

#### `testify/assert`:

1. If the statement fails, marks the test as failed.

2. **Does not interrupt** the execution of the current test.

3. Useful when you want to collect multiple independent inconsistencies in a
   single run.

#### `testify/require`:

1. If the assertion fails, marks the test as failed.

2. **Immediately stops** the current test (fail now).

3. Required for prerequisite checks without which the following steps are
   incorrect.

#### When to choose:

1. `require` — for critical preconditions:

- object is not `nil`;

- error is absent before further actions;

- input is prepared correctly.

2. `assert` — for postconditions and independent checks of the result.

#### Practical conclusion:

`require` controls the life cycle of the test, `assert` — diagnostic detailing.
A good test usually combines both: `require` for "stop conditions", `assert` for
further content control.

</details>


<details>
<summary>108. How does `t.Run` allow you to run subtests and filter them?</summary>

#### Go

`t.Run` allows you to structure a single test into a set of named subtests. Each
subcase is executed as a separate logical unit, which simplifies table tests,
diagnostics, and selective startup.

#### How `t.Run` works:

1. In the main test, `t.Run(name, func(t *testing.T) { ... })` is called.

2. Each call creates a separate subtest with its own `t`.

3. Subtests can have different inputs, assertions, and settings.

#### Why it is convenient:

1. **Better readability of table-driven tests.**

2. **Precise diagnostics:** you can see exactly which case fell.

3. **Test Hierarchy:** can be nested `t.Run` to group scenarios.

4. **Concurrency control:** individual subcases can be run via `t.Parallel()`.

#### How filtering works:

1. `go test -run <pattern>` runs tests whose names match the pattern.

2. Name path is taken into account for subtests (eg `TestXxx/case_name`).

3. This allows you to point-run a single problem case without a full set.

#### A practical example of thinking:

1. `TestParser` contains dozens of cases through `t.Run`.

2. Only one is run during debugging: `go test -run 'TestParser/invalid_header'`.

3. Get a faster feedback loop and a cleaner correction cycle.

#### Conclusion:

`t.Run` turns monolithic tests into a managed system of subtests with granular
triggering and filtering. This is one of the key tools of supported test design
in Go.

</details>


<details>
<summary>109. How to test HTTP handlers?</summary>

#### Go

HTTP handlers in Go are tested in isolation, without a real network socket,
using `httptest`. The goal is to test the HTTP layer contract: status, headers,
response body, error handling, and edge scenarios.

#### Canonical approach:

1. Create request via `httptest.NewRequest(...)`.

2. Create a recorder through `httptest.NewRecorder()`.

3. Call handler: `handler.ServeHTTP(rec, req)`.

4. Check:

- `rec.Code` (status code);

- headers;

- body (JSON/schema/message).

#### What must be covered:

1. **Happy path** (correct request, expected response).

2. **Validation errors** (incomplete/incorrect payload, query params).

3. **HTTP Methods** (GET/POST/PUT/DELETE + 405 if method not allowed).

4. **Dependency errors** (service/repository returns error).

5. **Contextual scripts** (timeout/cancel if the logic supports it).

#### Architectural tips:

1. Export business logic from the handler to the service layer.

2. In handler tests, mock/fake service dependencies.

3. Test the HTTP contract itself, not the internal implementation.

#### Practical minimum checks:

1. Correct `Content-Type`.

2. The structure of the JSON response.

3. Correspondence of status codes to domain errors.

4. No leakage of sensitive information in error-body.

#### Conclusion:

The HTTP-handler test in Go is a test of endpoint behavior as a black box:
incoming request → clear HTTP output. `httptest` provides a fast, deterministic
and reasonably accurate tool for such contract testing.

#### Example:

```go
req := httptest.NewRequest(http.MethodGet, "/health", nil)
rec := httptest.NewRecorder()

handler.ServeHTTP(rec, req)

if rec.Code != http.StatusOK {
	t.Fatalf("status=%d", rec.Code)
}
```

</details>


<details>
<summary>110. How to test for errors?</summary>

#### Go

Error testing in Go should check not only the fact that an error exists, but
also its semantics: type, category, wrapper chain, and expected system response.

#### What exactly to check:

1. **Presence/absence of an error** in a specific scenario.

2. **Error category** due to `errors.Is` (sentinel errors).

3. **Error type** via `errors.As` (custom error type with fields).

4. **Wrapper context** (whether the root cause is lost with `%w`).

5. **Behavioral effect**: correct status code, retry/no-retry, rollback, etc.

#### Recommended practices:

1. Avoid fragile full-text checks `err.Error()`.

2. For stable contracts, use `errors.Is/As`, not `==` for wrapped errors.

3. In table-driven tests, explicitly specify the expected error class and
   consequence.

#### What to test in negative scenarios:

1. Input validation errors.

2. Errors of external dependencies (DB, HTTP, queues).

3. Timeouts/Aborts via `context`.

4. Border states (empty values, incorrect formats, exceeded limits).

#### Architectural accent:

1. Error must be part of the API contract of the function.

2. Tests must prove that error handling is deterministic and predictable.

3. If the system maps domain errors to the transport layer, test this mapping
   separately.

#### Conclusion:

Qualitative error testing in Go is about checking the semantics, not the message
string. This kind of verification makes the code resistant to refactoring and
reliable in production.

</details>


<details>
<summary>111. How to wet external dependencies without using third-party frameworks?</summary>

#### Go

In Go, external dependencies are mocked most cleanly through interfaces and own
test-double implementations (stub/fake/spy), without the need for heavy mocking
frameworks. It's an idiomatic approach that scales well and remains transparent.

#### Basic scheme:

1. Highlight the minimum dependency interface in the consumer layer.

2. Production implementation works with real DB/HTTP/queue.

3. In the test, substitute your own structure that implements the same
   interface.

#### Test-double types without third-party libraries:

1. **Stub** — returns predefined data.

2. **Fake** - a simplified "working" implementation (for example, an in-memory
   repo).

3. **Spy** — captures calls (arguments, number, order).

4. **Manual mock** - Guided script with customizable responses/errors.

#### Advantages of this approach:

1. Complete type safety of the compiler.

2. Zero runtime magic.

3. Better test readability and predictable code evolution.

4. No external dependencies in the test stack.

#### Practical recommendations:

1. Make interfaces small (by behavior, not "on all methods").

2. Mot on module boundary, not inside domain logic.

3. For competitive scenarios, protect state test-double (`mutex`, atomics).

4. Do not duplicate the production logic in fake excessively - otherwise the
   tests become fragile.

#### Conclusion:

Mocking without frameworks in Go is primarily about good dependency design:
small interface + manual test-double. This approach is simple, reliable and
architecturally sound for long-term project support.

</details>


<details>
<summary>112. How to use `TestMain` to set up a test environment?</summary>

#### Go

`TestMain(m *testing.M)` is the entry point for the entire test suite. It allows
global initialization before tests and guaranteed cleanup after them.

#### When `TestMain` is appropriate:

1. Must raise the shared test environment once:

- test database/container;

- temporary directories;

- global configurations/secrets;

- background service dependencies.

2. Requires a centralized teardown after all package tests are complete.

#### Basic life cycle:

1. Setup is in progress (initialization of resources).

2. Tests run through `code := m.Run()`.

3. Cleanup is in progress.

4. Process terminates via `os.Exit(code)`.

#### Important rules:

1. `m.Run()` must be called exactly once.

2. The returned code must be passed to `os.Exit`, otherwise the status of the
   tests will be lost.

3. Cleanup should be performed even in case of setup errors (as far as
   possible).

4. Don't do extra logic in `TestMain` that is not related to the environment.

#### Practical tips:

1. Don't rely solely on `TestMain` to isolate tests within a package - local
   setup/teardown in specific tests is often still needed.

2. If possible, prefer lighter mechanisms (`t.Cleanup`) at test level;
   `TestMain` use for true batch context.

3. In parallel tests, carefully monitor the shared state initialized in
   `TestMain`.

#### Conclusion:

`TestMain` — test environment batch orchestration tool: one setup, one run of
all tests, one cleanup. It is appropriate where you need to control the life
cycle of shared resources for the entire package.

</details>


<details>
<summary>113. How to use golden files?</summary>

#### Go

`Golden files` are reference files with the expected output against which the
test compares the actual output. The approach is particularly useful for
formatter, code generators, serialization, and any text/structure output.

#### Basic workflow:

1. Generate the result with the tested function.

2. Read the corresponding `.golden` file.

3. Compare the actual output with the standard.

4. If there is a difference, the test fails with the diff.

#### Typical structure:

1. Test Input (`testdata/input/...`).

2. Standards (`testdata/golden/...`).

3. Table-driven tests, where each case has its own golden file.

#### Very useful practice — update mode:

1. Add a flag like `-update`.

2. If enabled, the test overwrites the golden files with the new result.

3. This speeds up support for benchmarks with legitimate behavior changes.

#### What to pay attention to:

1. **Determinism output:** before comparison, normalize the order of data,
   timestamps, random values.

2. **Qualitative diff:** in the test crash it should be clear what exactly
   changed.

3. **Do not abuse:** golden files for large "black boxes" without semantic
   checks can make diagnostics difficult.

#### When golden files are most appropriate:

1. Text rendering/generation.

2. JSON/XML/config transformation.

3. CLI-output.

4. Compilers, parsers, code generators.

#### Conclusion:

Golden files is a practical tool for contract output testing. Provided
determinism and a convenient update process, they provide quick and clear
protection against unwanted regressions in the result format.

</details>


<details>
<summary>114. How to properly test Go code that uses `time.Now()` so that the tests are deterministic?</summary>

#### Go

`time.Now()` makes the tests non-deterministic because it returns the actual
current time. For the tests to be stable, the time should be injected, not read
directly inside the business logic.

#### Canonical approach:

1. Export time source to dependency:

- function `now func() time.Time`;

- interface `Clock` with method `Now()`.

2. In production, transfer the real clock (`time.Now`).

3. Transmit a fixed time (fake clock) in the test.

#### Why it works:

1. The result does not depend on the moment the test is started.

2. Gone are the flaky "sometimes crashes, sometimes not" scenarios.

3. Easily check edge-cases: deadlines, TTL, transition dates, time zones.

#### Additional practices:

1. Do not compare time values with "hard" millisecond precision unless required
   by the domain.

2. For tests with timers/delays, use a controlled clock or sufficient time
   buffers.

3. Fix `Location/UTC` explicitly to avoid environment dependencies.

#### What not to do:

1. Leave `time.Now()` in the depth of the domain logic without the possibility
   of substitution.

2. Rescuing `time.Sleep`s in tests slows down and does not guarantee stability.

#### Conclusion:

Deterministic timing testing in Go is built on dependency inversion: timing is
an input, not a global side effect. Clock source injection makes tests fast,
reproducible, and architecturally clean.

</details>


<details>
<summary>115. How does `t.Parallel()` speed up the test suite and where can it break them?</summary>

#### Go

`t.Parallel()` allows tests (or subtests) to run concurrently, which typically
reduces overall runtime on multi-core environments. But concurrency without
isolation easily turns stable tests into flaky ones.

#### How it speeds up runs:

1. Independent tests run concurrently.

2. Better use of CPU and I/O waits.

3. A large set of small tests runs much faster in CI.

#### Where `t.Parallel()` can break tests:

1. **Shared mutable state:** global variables, shared in-memory caches, static
   configurations without synchronization.

2. **External shared resources:** one DB schema/table, one port, one file, one
   temporary data directory.

3. **Execution Order Dependency:** if a test implicitly expects another to have
   already run.

4. **Environment side effects:** changes to env vars, time zone, working
   directory without isolation.

5. **Bugs in table-driven subtests:** loop variable capture without local copy
   in closure.

#### How to use safely:

1. Parallel only fully isolated tests.

2. Avoid global mutable state or protect it with synchronization.

3. Use unique temporary resources (`t.TempDir`, individual fixtures).

4. For DB tests — transactional isolation or a separate namespace/schema per
   test.

5. Run the set with `-race` for early detection of competition issues.

#### Conclusion:

`t.Parallel()` is a powerful test accelerator, but only under strict case
isolation. If the tests have shared state or hidden dependencies, concurrency
will expose these defects and make the run unstable.

</details>


<details>
<summary>116. How to measure code coverage?</summary>

#### Go

In Go, code coverage is measured by built-in tools `go test` through test
execution instrumentation. This provides metrics that show what fraction of
lines/blocks of code were executed during the test run.

#### Basic commands:

1. Total coverage per package: `go test -cover ./...`

2. Coverage Profile Collection: `go test -coverprofile=coverage.out ./...`

3. View summary statistics: `go tool cover -func=coverage.out`

4. Highlighted HTML report: `go tool cover -html=coverage.out`

#### What is important to understand:

1. Coverage shows the fact that invariant checks are performed, not complete.

2. A high percentage does not guarantee the absence of bugs.

3. Low percentage is a signal of blind testing areas.

#### Practical tips:

1. Analyze coverage along with code criticality, not chasing "100%".

2. Cover negative and edge-case scenarios separately.

3. Use coverage as a gap indicator, not an end in itself.

4. In CI, save profile and track coverage dynamics between PRs.

#### Conclusion:

Code coverage in Go is measured by the standard tooling (`go test` + `go tool
cover`) and is a useful metric of test review quality. It provides the greatest
value in combination with semantic checks and meaningful test design.

</details>


<details>
<summary>117. What is benchmarking and how to run it? How does `testing.B` implement the benchmark and what does `b.ResetTimer` reset?</summary>

#### Go

`Benchmarking` in Go is a measurement of code performance (time, allocations,
throughput) under controlled conditions to compare implementations and validate
the effect of optimizations.

#### How to run the benchmark:

1. Functions have the form: `func BenchmarkXxx(b *testing.B)`.

2. Base Launch: `go test -bench=.`

3. Only specific benchmark: `go test -bench=BenchmarkParse`

4. Allocation measure: `go test -bench=. -benchmem`

#### How `testing.B` works:

1. Runner itself chooses `b.N` (number of iterations) to get a stable dimension.

2. Your code in the benchmark function is executed in a `for i := 0; i < b.N;
   i++` loop.

3. As a result, the test ranks performance in `ns/op`, and with `-benchmem` also
   `B/op`, `allocs/op`.

#### What `b.ResetTimer` does:

1. Reset the accumulated measurement timer.

2. Does not count preparation code executed before calling `ResetTimer` in the
   final time.

3. Used after the setup phase to measure only the "clean" working part.

#### Related useful methods:

1. `b.StopTimer()` / `b.StartTimer()` — temporarily disable/enable timekeeping.

2. `b.ReportAllocs()` — force allocation statistics.

#### Practical conclusion:

Benchmark in Go is not a one-time run, but a comparison tool under the same
conditions. `testing.B` automatically scales iterations, and `b.ResetTimer`
separates training from actual performance measurement.

#### Example:

```go
func BenchmarkParse(b *testing.B) {
	input := []byte(`{"x":1}`)
	b.ResetTimer()

	for i := 0; i < b.N; i++ {
		var v map[string]int
		_ = json.Unmarshal(input, &v)
	}
}
```

</details>


<details>
<summary>118. How to run benchmarks with control of time and number of iterations?</summary>

#### Go

In Go, benchmarks can be run with control of the measurement duration and a
fixed number of iterations via the `go test` parameters. This is important for
reproducibility and correct comparison of results.

#### Main flags:

1. **`-benchtime`**

- sets the duration of the benchmark run (for example, `-benchtime=5s`);

- runner itself picks `b.N` to run around this time window.

2. **`-benchtime=Nx`**

- fixes the exact number of iterations (for example, `-benchtime=100000x`);

- handy for reproducible A/B comparisons on the same `N`.

3. **`-count`**

- number of reruns (eg `-count=10`);

- helps to assess the stability and dispersion of the results.

4. **`-bench`**

- selection of specific benchmark functions by pattern.

5. **`-benchmem`**

- additionally outputs allocations (`B/op`, `allocs/op`).

#### Practical examples of scenarios:

1. Longer stable run: `go test -bench=. -benchtime=5s -benchmem`

2. Fixed `N`: `go test -bench=BenchmarkFoo -benchtime=200000x -benchmem`

3. Multiple replays for stats: `go test -bench=BenchmarkFoo -benchtime=2s
   -count=10`

#### Why is it necessary:

1. Reduce the noise of short runs.

2. Compare optimizations under the same conditions.

3. Receive statistically meaningful data for `benchstat` analysis.

#### Conclusion:

Control of time and iterations in Go benchmarks is a prerequisite for
high-quality performance analysis. `-benchtime` and `-count` provide measurement
stability, and `Nx` mode provides strict control over the number of executions.

</details>


<details>
<summary>119. How does the `benchstat` tool compare two sets of benchmark results and how does it determine the significance of changes?</summary>

#### Go

`benchstat` compares two (or more) sets of benchmark results and shows whether
changes in metrics (`ns/op`, `B/op`, `allocs/op`) are statistically significant
and not random run noise.

#### How the comparison works:

1. Collect multiple "before" and "after" runs (usually via `-count`).

2. `benchstat` groups results by the same benchmark names.

3. Computes central values ​​(typically median-like/robust estimates) and
   percent difference.

4. Performs a statistical test and outputs `p-value`.

#### How significance is determined:

1. If `p-value` is below a threshold level (typically 0.05), the change is
   considered statistically significant.

2. If `p-value` is above the threshold, the difference may be environmental
   noise.

3. That's why it's important to look at **both delta and p-value** at the same
   time.

#### What is needed for a correct analysis:

1. Same launch conditions (machine, load, configuration).

2. Sufficient number of repetitions (`-count`) otherwise conclusions are
   fragile.

3. No extraneous noise (background processes, thermal throttling, unstable CI
   environment).

#### Rule of thumb:

1. Don't trust disposable `go test -bench`.

2. Collect series of before/after results.

3. Analyze through `benchstat` and then check if the change is important to
   business metrics (latency/throughput/SLA) and not just "pretty" in a table.

#### Conclusion:

`benchstat` converts raw benchmark numbers into a statistically sound
comparison. It helps to distinguish a real performance effect from a random
scatter and to make engineering decisions based on data.

</details>


<details>
<summary>120. What is fuzz testing?</summary>

#### Go

`Fuzz testing` is an automated testing method where the system receives a large
amount of semi-random or mutated input data to detect crashes, panics, incorrect
edge-case handling, and invariant violations.

#### How it works in Go:

1. Set the fuzz function (`func FuzzXxx(f *testing.F)`).

2. Add seed entries (initial examples).

3. The fuzzer mutates these inputs and generates new combinations.

4. If it finds a crash or check violation, keep the "minimum" playable case.

#### What fuzz testing finds best:

1. Unexpected edge-cases of parsers/decoders.

2. Panics on incorrect or "broken" input data.

3. Logical defects in the processing of lines, bytes, formats, protocols.

#### Why it is valuable:

1. Covers the input space much wider than manual unit cases.

2. Good at detecting security flaws in parser-like code.

3. Adds API resistance to "toxic" payloads from the outside world.

#### Practical recommendations:

1. Formulate explicit invariants (which must be true for any input).

2. Start with critical surfaces: parsing, deserialization, normalization.

3. After finding a case, add it as a regression test.

4. Combine fuzzing with `-race` and regular unit/integration tests.

#### Conclusion:

Fuzz testing in Go is a systematic way to "break" the code with input data to
find defects that are almost impossible to predict manually. It is one of the
most powerful tools for increasing the reliability and security of data
processing.

</details>


<details>
<summary>121. What are the ways to run tests from the DB in CI (Testcontainers, docker-compose, GitHub Actions services)? What are the advantages of each approach?</summary>

#### Go

For integration tests with DB in CI, three approaches are most often used:
`Testcontainers`, `docker-compose` and `GitHub Actions services`. The choice
depends on the level of isolation you want, the complexity of the stack, and the
speed of the pipeline.

#### 1) Testcontainers

**Gist:** containers are raised programmatically from tests and live within the
test run.

**Advantages:**

1. Maximum proximity to test code (infra described next to tests).

2. High case isolation and predictable environment.

3. Flexible management of the database life cycle, versions, init scripts.

4. Convenient for local reproduction of CI scripts.

#### 2) docker-compose

**Essence:** services (DB + dependencies) are described in `docker-compose.yml`,
are raised before the tests as a single composition.

**Advantages:**

1. A simple and visual description of a multi-service environment.

2. It is easy to add caches, brokers, several DBs at the same time.

3. Same model for local dev and CI.

4. Good choice for integration/e2e kits.

#### 3) GitHub Actions services

**Gist:** the DB container is declared directly in the workflow job as a service
container.

**Advantages:**

1. The simplest CI-native script for basic needs.

2. Minimum code in tests and separate orchestration.

3. Quick start for one or two services (Postgres, Redis, etc.).

#### Practical comparison:

1. **Flexibility and isolation**: Testcontainers > docker-compose > services.

2. **Easy to start**: services > docker-compose > Testcontainers.

3. **Multi-service composite stands**: docker-compose / Testcontainers.

4. **Laconic CI for simple DB**: GitHub Actions services.

#### Conclusion:

There is no universally "best" approach. For a simple CI, services are enough;
docker-compose is appropriate for a complex integration environment; for the
most manageable and reproducible tests at the code level, the strongest approach
is Testcontainers.

</details>


<details>
<summary>122. What is `go vet`?</summary>

#### Go

`go vet` is a static analyzer from the standard Go toolchain that looks for
suspicious code constructions, which are often logic errors but may not be
caught by the compiler.

#### What `go vet` checks for:

1. Mismatch of format strings and arguments (`Printf`-like calls).

2. Suspicious errors with copying lock objects.

3. Problematic work patterns with `testing`, `atomic`, `struct tags`, etc.

4. Other common defects that may compile but break behavior.

#### How `go vet` differs from the compiler:

1. The compiler checks the correctness of syntax and types.

2. `vet` checks for "suspicious intent" and anti-patterns.

3. That is, it is not a replacement for tests, but an additional level of
   quality.

#### How to run:

1. For the current package: `go vet`

2. For the entire module: `go vet ./...`

#### Practical role in the project:

1. Regularly run locally before commit.

2. Add to CI as a mandatory quality gate.

3. Consider warning `vet` as a signal for careful code review.

#### Conclusion:

`go vet` is an early detection tool for insidious bugs. It improves code
reliability by complementing the compiler and tests, especially in large team Go
codebases.

</details>


<details>
<summary>123. How to profile a Go application (`pprof`)?</summary>

#### Go

`pprof` is a standard Go profiling tool that shows where CPU, memory,
allocations, locks, and timeouts are going. This is a basic way to find real
bottlenecks before optimizations.

#### What can be profiled:

1. **CPU profile** — where CPU time is spent.

2. **Heap / allocs** — who allocates memory and what remains "alive".

3. **Goroutine profile** — state and number of goroutines.

4. **Block / mutex profile** — contention, blocking, synchronization delays.

#### How to connect in the service:

1. Import `net/http/pprof` (usually via side-effect import).

2. Open debug endpoint (often a separate port or protected route).

3. Remove profile under real/representative load.

#### Typical analysis workflow:

1. Collect CPU/heap profile.

2. Open via `go tool pprof` (top/list/web).

3. Find hot paths/allocation nodes.

4. Make a point change.

5. Repeat profiling and compare before/after.

#### Practical teams (general idea):

1. Collection of profile from endpoint.

2. Local analysis: `go tool pprof <profile>`

3. Graph/flame-like visualization via web mode.

#### Important principles:

1. Do not optimize "by feeling" - only according to profile data.

2. Profile under conditions close to production.

3. Check if optimization has not degraded other metrics (tail-latency, memory).

#### Conclusion:

`pprof` is the main tool for proof-of-concept optimization of Go applications:
it shows the real picture of costs and allows you to make engineering decisions
based on measurements, not intuition.

</details>


<details>
<summary>124. How does `go build` and cross-compilation work?</summary>

#### Go

`go build` compiles Go packages/programs into a binary (or verifies assembly)
using module dependencies, the build cache, and current target platform
settings.

#### How `go build` works:

1. Reads `go.mod` and resolves dependencies.

2. Compiles the required packages (taking into account build tags and
   conditional files).

3. Uses build cache to speed up re-builds.

4. Links the final executable for the target OS/architecture.

#### What is cross-compilation:

Cross-compilation is building a binary for a different platform than the one
you're running the compiler on.

#### Main parameters:

1. `GOOS` is the target operating system (eg `linux`, `darwin`, `windows`).

2. `GOARCH` is the target architecture (`amd64`, `arm64`, etc.).

#### Example:

1. Working on macOS.

2. Want Linux/amd64 binary.

3. Compiled with the corresponding `GOOS/GOARCH`, you get an artifact for Linux
   deployment.

#### Practical nuances:

1. For pure-Go code, cross-compilation is usually straightforward.

2. The `cgo` dependencies require a compatible cross-toolchain (C compiler for
   the target platform).

3. CI often do a matrix-build for the set `GOOS/GOARCH`.

#### Conclusion:

`go build` is a standardized build with caching and modular resolution.
Cross-compilation in Go is natively supported through `GOOS/GOARCH`, which makes
the language very convenient for multi-platform releases.

</details>


<details>
<summary>125. How to containerize a Go application in Docker?</summary>

#### Go

Containerizing a Go application is building a binary and packaging it into a
Docker image for predictable launch in any environment (on-premises, CI,
Kubernetes, cloud).

#### Canonical approach:

1. Use multi-stage Dockerfile:

- stage build: Go binary compilation;

- stage runtime: Minimum image to run.

2. At the build stage:

- copy `go.mod/go.sum`, load dependencies;

- copy code;

- compile the binary (`go build`).

3. At the runtime stage:

- put only the final binary and necessary runtime files;

- set `ENTRYPOINT/CMD`.

#### Why it's right:

1. Smaller final image size.

2. Better security (fewer redundant packages at runtime).

3. Reproducible builds in CI/CD.

4. Faster deployment and cold start.

#### Practical recommendations:

1. Add `.dockerignore` to avoid pulling extra files into the build context.

2. Run the process as a non-root user in the runtime image.

3. Explicitly set `EXPOSE`, healthcheck (if needed) and environment variables.

4. Use pinned base image/tag for predictability.

#### Typical life cycle:

1. `docker build` → received an image.

2. `docker run` → checked locally.

3. Push to the registry → deploy to the target environment.

#### Conclusion:

Containerizing a Go application in Docker works best through a multi-stage
approach: compile separately, execute separately. This gives a compact, safe and
operationally convenient production image.

</details>


<details>
<summary>126. How to reduce the size of a Docker image for a Go application (multi-stage build)?</summary>

#### Go

The most effective way to reduce the image of a Go application is multi-stage
build: compile in a "heavy" build image, and run in the most minimal runtime
image with only the final binary.

#### Key optimization steps:

1. **Multi-stage Dockerfile**

- stage 1: `golang` for assembly;

- stage 2: slim runtime (`distroless`/`scratch`/minimum base).

2. **Only necessary to copy in runtime**

- binary;

- if necessary CA-certs / timezone data / config.

3. **Static binary (where appropriate)**

- reduces runtime dependencies;

- is good for minimal looks.

4. **Optimize the binary itself**

- linker flags (`-ldflags="-s -w"`) to reduce service information.

5. **Literate `.dockerignore`**

- remove tests, `.git`, artifacts, local caches from build-context.

6. **Dependency caching in the build stage**

- copy `go.mod/go.sum` separately before copying the entire code.

#### Additional practices:

1. Foam base images by digest/tag for reproducibility.

2. Work under a non-root user.

3. Regularly check image size and vulnerabilities in CI.

#### What to avoid:

1. Runtime on a full `golang` image is unnecessary.

2. Copying the source code to the final layer.

3. Redundant debugging tools in the production image.

#### Conclusion:

A compact Go image is the result of proper segregation of build/runtime layers.
Multi-stage + minimal runtime + clean build context give the best balance of
size, security and deployment speed.

</details>


<details>
<summary>127. What tools are commonly used to collect metrics and logs? How does Prometheus work?</summary>

#### Go

Modern systems usually combine several classes of tools: metrics, logs, tracing,
visualization, and alerting. This gives a complete picture of the service's
behavior and speeds up the diagnosis of incidents.

#### Typical tool stack:

1. **Metrics**

- Prometheus, VictoriaMetrics, Graphite (less common in newer systems).

2. **Visualization**

- Grafana (dashboards, SLOs, metrics correlation).

3. **Logs**

- Loki, Elasticsearch/OpenSearch + Kibana, Fluent Bit/Fluentd, Vector.

4. **Tracing**

- OpenTelemetry + Jaeger/Tempo/Zipkin.

5. **Alert**

- Alertmanager (often associated with Prometheus).

#### How Prometheus works:

1. **Pull collection model:** Prometheus periodically "scrapes" the HTTP
   endpoints of services (usually `/metrics`) and takes the current values of
   the metrics.

2. **Time-series storage:** each metric with a set of labels is stored as a time
   series.

3. **PromQL queries:** aggregation, rate functions, percentile-like analytics,
   correlations.

4. **Rule engine:**

- recording rules for preliminary calculations;

- alerting rules for generating alerts.

5. **Integration with Alertmanager:** deduplication, routing, grouping and
   notifications (Slack, email, PagerDuty).

#### Why Prometheus is popular:

1. Simple operational model (pull + configuration files).

2. Powerful PromQL.

3. A large ecosystem of exporters.

4. Good integration with Kubernetes and cloud-native environment.

#### Conclusion:

For metrics and logs, production usually uses a combined stack: Prometheus +
Grafana for metrics, a separate log platform for logs, and tracing for
cross-service diagnostics. Prometheus in this stack acts as a time-series
monitoring and alerting core.

</details>


<details>
<summary>128. What is the difference between microservices and a monolith? What are the advantages and disadvantages?</summary>

#### Go

Monolith and microservices are not "fashion", but different strategies of system
decomposition. The choice between them is determined by team size, domain
complexity, release autonomy requirements, and operational maturity.

#### Monolith:

**Gist:** one application, one code base (or tightly coupled runtime), usually
one deployment point.

**Advantages:**

1. Easy start and lower operational complexity.

2. Easier local debugging and in-process transactional integrity.

3. Faster development for small teams/early stage products.

**Disadvantages:**

1. It is more difficult to scale individual "hot" modules independently.

2. As code grows, so does connectivity and the risk of slow releases.

3. One large deployment makes frequent independent changes difficult.

#### Microservices:

**Gist:** the system is divided into autonomous services with their own limits
of responsibility, API-contracts and independent life cycle.

**Advantages:**

1. Independent releases of teams and services.

2. Point scaling of individual components.

3. Technological flexibility at the service level (with governance).

**Disadvantages:**

1. High operational complexity (network, discovery, observability, security).

2. Distributed consistency and complex inter-service transactions.

3. More expensive to debug due to network interaction and more moving parts.

#### Practical conclusion:

A monolith is often the best start and can be quite effective for a long time.
Microservices are justified when the scale of the domain and organization really
needs the autonomy of teams, independent scaling and clear service
decomposition.

</details>
