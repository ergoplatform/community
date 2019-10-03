## Code Testing Guide

### Motivation

You have to be inspired by the mission of the blockchain network: 
[open, public, borderless, neutral, and censorship resistant](https://www.youtube.com/watch?v=qlAhXo-d-64).
Technically this is based on the consensus protocol in a massively 
distributed network of peer-to-peer nodes. 

From software development point of view, the most important thing is to not 
break the consensus on the network, and provide a guarantee of backward compatibility 
when rolling out new releases. 

Because the Ergo network has those five pillars, there can be many different versions 
running at the same time which must behave "observably the same" the following should 
be guaranteed:
1) New releases don't accidentally break Ergo protocol (i.e. behave correctly)
2) All public APIs preserve backward compatibility to not break existing application.
3) Application is free to choose any node on the network to communicate with, thus
all the nodes should have equivalent observable behavior.

### Practices

Better test coverage doesn’t mean more tests, it means that all aspects are tested, 
focusing primarily on regression, so that the semantics do not change in a new version. 
Otherwise the new version will end up breaking the consensus in the network and/or 
breaking existing applications.

Each API method needs to be covered with tests, including those that catch regression.
Since the method is public applications can use it after we release it for the first time. 

Before every new release, we need to be sure that the semantics of all API methods have 
not changed. Tests can give some degree of confidence, but no guarantee.
Every developer is expected to think creatively and seriously to come up with good
tests which are granular, easy to understand and "catching for regression bugs efficiently".
We have some testing infrastructure, but it is far from ideal so contributions are very welcome. 

Writing new tests and thinking about test coverage is the task of the developer of a new feature.
The project do not have full-time testers at this stage (though volunteers are welcome). 

[Ergo reference implementation](https://github.com/ergoplatform/ergo) has unit and integration
tests more or less covering all aspects of the system.
There is always some level of technological debt as the project goes forward.  
And it will be necessary to refactor a lot, for this, again, tests will be needed 
which help localize the problem, i.e. we need granular tests, and we need tests 
able to catch regression bugs.

Now the system is at the stage of improving and cleaning up of the implementation 
of Ergo Protocol v1. At the same new features are constantly being added, 
roughly (50% + 50% of team efforts).

Test coverage requirements need to be increased, i.e. not only to add more tests 
for existing features, but also for new ones to have better coverage.

### In summary

- Rule 1: New release shouldn't break protocol and consensus
- Rule 2: Testing is highly valuable and respected and part of software development (because of Rule 1)
- Rule 3: More tests doesn't mean better test, focus on coverage and catching potential bugs
- Rule 4: Every developer is encouraged to take it seriously and creatively
- Rule 5: Reviewers should enforce this rules and reject code with is not well covered with tested.
