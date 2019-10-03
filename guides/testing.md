## Code Testing Guide

### Motivation

In order to partake in this project you must be inspired by the true mission of blockchains in being 
[open, public, borderless, neutral, and censorship resistant](https://www.youtube.com/watch?v=qlAhXo-d-64).
Meeting these goals is possible thanks to the consensus protocol which is run on a massively 
distributed network of peer-to-peer nodes. 

From the software development point of view, the most important thing is to not 
break the consensus on the network, and thus provide a guarantee of backward compatibility 
when rolling out new releases. 

Because the Ergo network abides by the previously mentioned five pillars, it is possible that there may be different versions 
running at the same time, yet they must all behave "observably the same". What this means in practical terms is that the following should 
be guaranteed:
1) New releases don't accidentally break the Ergo protocol.
2) All public APIs preserve backward compatibility so existing applications never become obsolete.
3) Applications should be free to communicate with any node on the network, thus
all nodes should behave equivalently.

### Practices

Better test coverage doesn’t mean more tests, it simply means that all aspects are tested. 
This is possible by focusing primarily on regression, so that the semantics do not change in new versions. 
If the semantics do change in new versions they will end up breaking the consensus on the network and/or 
break compatibility with existing applications.

Each API method needs to be covered with tests, including those that catch regression.
Since the methods are public, applications will use them once they are released for the foreseeable future.

Therefore before every new release we need to ensure that the semantics of all API methods have 
been kept in tact. Tests can give some degree of confidence, but they are no guarantee.
Each developer is expected to think creatively and seriously when it comes to creating good
tests which are granular, easy to understand, and "catch regression bugs efficiently".
We have some testing infrastructure, but it is far from ideal so contributions are very welcome. 

Writing tests and thinking about test coverage is the responsibility of the developer who is implementing a new feature.
The project does not have full-time testers at this stage, though volunteers are welcome, so make sure to do a good job in the first place. 

[The Ergo reference implementation](https://github.com/ergoplatform/ergo) has unit and integration
tests which more or less cover all aspects of the system.
There is always some level of technological debt as projects develop and move forward. 
Inevitably it will be necessary to refactor a lot, which again will require tests to
aid in locating problems (i.e. we need granular tests, and tests 
which catch regression bugs).

The project is at a stage of improvement and cleaning up of the original implementation 
of the Ergo Protocol v1. That being said, new features are also constantly being added, 
roughly at a rate of 50% cleanup and 50% new additions.

Test coverage requirements need to be increased as we progress forward, not only by adding more tests 
for existing features, but also for new features to have better coverage from the get-go.

### In summary

- Rule 1: New releases shouldn't break the protocol nor consensus
- Rule 2: Testing is an extremely vital and valued part of the software development process (because of Rule 1)
- Rule 3: More tests doesn't mean better tests, focus on coverage and catching potential bugs rather than hitting a high count of tests.
- Rule 4: Every developer is encouraged to take testing seriously and to be as creative as possible.
- Rule 5: Reviewers should enforce these rules and reject code which does not have good test coverage.
