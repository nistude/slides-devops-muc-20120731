!SLIDE subsection incremental

# Infrastructure Coding #
## Why think about testing? ##

* **fast** feedback that it **works** (initially)
* **fast** feedback that it **still works** (refactoring)

!SLIDE subsection incremental

# Infrastructure Coding #
## How to verify that it works? ##

* run chef/puppet on the target node
* verify service functionality
* **comprehensive** but **slow**
* Can we do better?

!SLIDE subsection incremental

# Infrastructure Coding #
## What are we testing? ##

* syntax (does it compile?)
* execution (does it do what we want?)
* service (does it work as expected?)

!SLIDE subsection incremental

# Syntax Checks #
## Puppet ##

* `puppet parser validate`
* `puppet-lint`
* **focused** and **fast**

!SLIDE subsection incremental

# Syntax Checks #
## Chef ##

* `knife cookbook test`
* `foodcritic`
* **focused** and **fast**

!SLIDE subsection incremental

# (Pre-) Execution Tests #

* `cucumber-puppet`
* `rspec-puppet`
* `chefspec` (`rspec-chef`)
* what do they actually test?

!SLIDE subsection incremental

# (Pre-) Execution Tests #

* don't cover all aspects of the execution stage, e.g. files
* don't cover complicated environments, e.g. directory existence
* danger of useless double-entry bookkeeping

!SLIDE subsection incremental

# Test-Driven Development #

* develop code test-first
* acceptance tests (cucumber)
* unit tests (MiniTest, RSpec, Test::Unit)
* test certain aspects of an application in isolation

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
* a design activity, tests are incidental

!SLIDE subsection incremental

# So What? #

* TDD's goal is design, not testing
* infrastructural code has different demands than program code
  * declarative vs. imperative
  * while the business model is in the communication patterns of objects,
    infrastructure results from the interaction of resources with an
    environment

!SLIDE subsection incremental

# (Pre-) Execution Tests #

* I don't see much value in using existing tools
* I believe infrastructure is different enough to warrant its own set of tools

!SLIDE subsection incremental

# Service Tests #

* `cucumber-chef`, `toft`, et al.
* `minitest-chef-handler`
* danger of testing chef/puppet internals
* monitoring
* **comprehensive** but **slow**

!SLIDE subsection incremental

# Conclusion #

* unit testing makes sense for reusable components like custom resources
* infrastructural code should be linted for low-level qualities (syntax, style)
* infrastructural code needs to be integration tested (monitoring) for
  functional qualities
