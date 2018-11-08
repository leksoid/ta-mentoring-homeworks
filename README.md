# Lesson 1 HW #
- - - -
#### Answer the following questions

  1. Is it necessary to set up test automation processes for your SUT? Why?
  2. What should/could be automated for your SUT? Why? How?

##### Answers

1. _Is it necessary to set up test automation processes for your SUT? Why?_

  Given the current SUT, it is very necessary to have an automation processes in place, according to following reasons:
    * frequent manual execution
      * several times a week for a smoke testing of the environment
      * twice a week doing a full regression on integrated team deployments
      * potential daily production releases of some projects
    * TCs constantly increasing in the total amount, as new features being implemented
    * some of the TCs are expensive to run manually, as they involve complex verification of data from APIs and DBs

  Having the automation of majority of TCs in place, would save the time of manual QAs and provide with possibility to perform more of the non-functional testing.

2. _What should/could be automated for your SUT? Why? How?_

  * Smoke testing should be automated in first place, given that it requires execution several time a week after the build is done by dev team to insure that major piece of functionality is working as expected. The tests can be triggered by some event, so dev team could get the report right away, without even passing the task to QA team.
  * Regression testing is also a top priority, given the amount of TCs. There are several of other teams working on the project, so even their changes to code base would result if defects if some component are shared between them.
  * All tests that require lots of data verification can be error-prone when done by human. This can be done by API or DB testing, validating the data on backend. This tests usually fast to execute.

##### Calculate ROI (return on investment) value for your SUT. Provide rationale for your calculations with assumptions and description for each step.
