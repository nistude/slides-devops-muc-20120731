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
* danger of useless double-entry bookkeeping

!SLIDE subsection incremental

# Service Tests #

* `cucumber-chef`
* `minitest-chef-handler`
* danger of testing chef/puppet internals
* monitoring
* **comprehensive** but **slow**
