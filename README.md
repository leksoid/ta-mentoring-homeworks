# Lesson 2 HW 

#### Answer the following questions

  1. Is it necessary to set up test automation processes for your SUT? Why?
  2. What should/could be automated for your SUT? Why? How?

##### Answers

1. _Is it necessary to set up test automation processes for your SUT? Why?_

Given the current SUT, it is very necessary to have an automation processes in place, according to following reasons:

* frequent manual execution
 * several times a week for a smoke testing of the environment
 *  twice a week doing a full regression on integrated team deployments
 * potential daily production releases of some projects
* TCs constantly increasing in the total amount, as new features being implemented
* some of the TCs are expensive to run manually, as they involve complex verification of data from APIs and DBs

Having the automation of majority of TCs in place, would save the time of manual QAs and provide with possibility to perform more of the non-functional testing.

2. _What should/could be automated for your SUT? Why? How?_


 * Smoke testing should be automated in first place, given that it requires execution several time a week after the build is done by dev team to insure that major piece of functionality is working as expected. The tests can be triggered by some event, so dev team could get the report right away, without even passing the task to QA team.
 * Regression testing is also a top priority, given the amount of TCs. There are several of other teams working on the project, so even their changes to code base would result if defects if some component are shared between them.
 * All tests that require lots of data verification can be error-prone when done by human. This can be done by API or DB testing, validating the data on backend. This tests usually fast to execute.

##### Calculate ROI (return on investment) value for your SUT. Provide rationale for your calculations with assumptions and description for each step.


To calculate ROI for an automation testing implementation we have a formula  
**ROI = (Cm – (FW+S+ER)) / (FW+S+ER)**,  
where
- Cm – manual testing cost (we will take total amount of hours to perform smoke and regression testing of TCs)
- FW – framework implementation cost
- S - test automation scenarios implementation cost (we will take an average of 3 hours for a 1 TC of medium complex flow when we have a framework created)
- ER – maintenance and report analysis cost

Given we have a long-term project of at least 5 years duration
With a total number of complex test cases to cover = 1300 (the estimated amount based on real numbers of the TCs in the team (currently ~800) , accumulated for past 3 years).

Cm = (Total hours spent on regression TR)+(Total hours spent on smoke testing TS)
* where TR = (2 x 8 x 3 x 2)x12x5 (2 qa's spending 8 hours 2/month for 5 years)
* where TS = (2 x 3 x 3 x 4)x12x5 (2 qa's spending 3 hours 3/week for 5 years)

| Variable      | Hours |
| --------- | -----:|
| Cm | 10080 |
| FW  | 80 |
| S     |   1300 TCs x 3 hours = 3900 |
| ER      |    8 hours x 52 weeks x 5 years = 2080 |

![](http://barnraisersllc.com/wp-content/uploads/2012/11/show-me-ROI.jpeg)

Considering this  
ROI = (10080-(80+3900+2080)/(80+3900+2080))x100%=66%

We will have a positive 66% ROI when we cover 100% of our regression testing and have a smoke tests run automatically.

If we want to cover only high priority TCs (typically is about 50% of all TCs = 650),  
ROI = (4320-(80+1950+1040)/(80+1950+1040))x100%=41%
