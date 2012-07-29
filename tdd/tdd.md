!SLIDE subsection incremental

# Test-Driven Development #

* develop code test-first
* acceptance tests (cucumber)
* unit tests (MiniTest, RSpec, Test::Unit)
* **comprehensive** and **fast**

!SLIDE subsection incremental

# Test-Driven Development #
## Acceptance Tests ##

* figure out what to build
* it's all about communication
* a reminder of a conversation

!SLIDE subsection incremental

# Test-Driven Development #
## Unit Tests ##

* figure out how to build it
* supports object-oriented design
* *listen to the tests*
* is a design activity
* tests are incidental

!SLIDE subsection incremental

# So What? #

* TDD tools are written for a specific purpose, which is **not** testing
* infrastructural code has different demands than program code
  * declarative vs. imperative
  * while the business model is in the communication patterns of objects,
    the infrastructure results from the interaction of resources

!SLIDE subsection incremental

# Conclusion #

* unit testing makes sense for reusable components like custom resources
* infrastructural code should be linted for low-level qualities (syntax, style)
* infrastructural code needs to be integration tested (monitoring) for
  functional qualities
