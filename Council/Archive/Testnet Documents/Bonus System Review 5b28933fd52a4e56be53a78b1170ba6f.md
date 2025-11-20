# Bonus System Review

**Pre-proposal Discussion thread - [https://dao.joystream.org/#/forum/thread/573](https://dao.joystream.org/#/forum/thread/573)**

### **Summary**

Changes to the Bonus System: 

1. Increase the weight of bonuses in overall Lead's compensation 
2. Introduce new mechanics which will help to implement the Bonus System.

### **Motivation**

Changes in the Bonus System are needed in order to make it more balanced. Leads are not really motivated to achieve targets specified in the Bonus System. Token rewards provided by the Bonus System are too low.

See the example:

> Bonus for the Lead for completing dozens of different tasks is about 270k-300k tJoy. Let's suggest, that Lead's extra hour's reward rate is 0.3M/hour.
> 

Here is a question. If a Lead wants to maximize his earnings, what will be his best strategy?

### **Specification**

The following changes in the Bonus System are supposed to be implemented:

**(1) Increase the weight of bonuses in overall Lead's compensation.**

> Let's define the current Lead's compensation (fixed salary) per the term as X.
> 
- Increase the new total or maximum Lead's compensation to 1.2 X. This is necessary to implement in order to make the new Lead's compensation comparable with the compensation for the previous terms.
- 50% of 1.2X will be covered by the fixed salary
- 50% of 1.2X will be covered by the bonus part

Example:

If Lead completes Bonus tasks for 80%, he will receive 0.6X+0.6X*0.8= 1.08X.

**(2) Introduce new mechanics which will help to implement the Bonus System**

It's proposed to limit the extra hour's compensation to 50% of submitted hours if the Bonus scores for the period are less than 50%. If the Lead has spare time for the extra work he should focus on the Bonus tasks first, and on his side tasks as the second priority.

### **Comment**

50% that frequently appears in the test is just a random number that should be adjusted due to the course of Bonus System development. Though it looks quite good for me.

***If you have a catastrophic error, you have bonuses canceled for the period.**

### HR

The group leader's current salary is 18 tJOY/block.
This is 1.8144 M tJOY/7 days
Max bonuses is 0.5 M tJOY
The total possible reward is 2.3144 M tJOY

From the description of the new bonus system, the maximum reward can be 2.3144х1.2=2.77728 M tJOY
1.38864 M tJOY will be covered by the fixed salary - 13.8 tJOY/block 
1.38864 M tJOY will be covered by the bonus part

Bonuses (max 1.38864 M tJOY**)***

- **Catastrophic Errors**
    - [ ]  Late summary (>6 hours or more)
    - [ ]  Late report (>6 hours or more)
    - [ ]  Late plan (>6 hours or more)
    - [ ]  No openings existed during the term
    - [ ]  Inadequate Report
    - [ ]  Missing Judgement
- **WG Period Plan** - max 138.864 k tJOY
    - [ ]  Publish on Forum according to deadline - 27.864 k tJOY
    - [ ]  4 Points/Lines should be made - 83 k tJOY
    - [ ]  5 Points/Lines should be made - 111 k tJOY
- **WG Summary** - max 138.864 k tJOY
    - [ ]  Publish on Forum according to deadline - 27.77 k tJOY
    - [ ]  All (8) Points/Lines should be done - 83.318 k tJOY
    - [ ]  Ideas to improve your Working Group were suggested - 13.888 k tJOY
    - [ ]  Ideas to improve other Working Group, Council, Jsgenesis ****were suggested - 13.888 k tJOY
- **WG Opportunities** - max 138.864 k tJOY
    - [ ]  Hire 10% of new workers from the current number of workers - 69.432 k tJOY
    - [ ]  Hire 20% of new workers from the current number of workers - 138.864 k tJOY
- **Bounty Score** - max 138.864 k tJOY
    - [ ]  Come up with one new bounty idea for newcomers - 138.864 k tJOY
- **Opening Score -** max 138.864 k tJOY
    - [ ]  No "downtime" without any openings, even just after filling or closing the old one - 46.288 k tJOY
    - [ ]  Quality of opening, in terms of information, requests, questions and contact details - 46.288 k tJOY
    - [ ]  There should be a forum thread to discuss the candidates - 46.288 k tJOY
- **Report Score -** max 138.864 k tJOY
    - [ ]  Publish on Forum according to deadline - 27.864 k tJOY
    - [ ]  8 points must be fulfilled - 111 k tJOY
- **Person Logging Score -** max ****138.864 k tJOY
    - [ ]  Added 50% of users - 56 k tJOY
    - [ ]  Added 75% of users - 111 k tJOY
    - [ ]  Added 100% of users - 138.864 k tJOY
    - [ ]  if the information is doubled - minus 28 k tJOY
- **Interaction Logging Score -** max ****138.864 k tJOY
    - [ ]  Added 50% of users - 56 k tJOY
    - [ ]  Added 75% of users - 111 k tJOY
    - [ ]  Added 100% of users - 138.864 k tJOY
- **Bounty Management Score -** max 138.864 k tJOY
    - [ ]  bounty_sum > 20 - 83 k tJOY
    - [ ]  bounty_sum > 30 - 111 k tJOY
    - [ ]  bounty_sum > 40 - 138.864 k tJOY
- **Response Time Score** - max 138.864 k tJOY ([An example of how to count it](https://www.notion.so/Response-Time-ac565bd2831a451d99d8163659887fdf?pvs=21))
    - [ ]  RESPONSE_TIME_SCORE = 0.6 - 69 k tJOY
    - [ ]  RESPONSE_TIME_SCORE = 0.8 - 111 k tJOY
    - [ ]  RESPONSE_TIME_SCORE = 1 - 138.864 k tJOY
    
    ## Action Items [25-Aug-2022]
    
    1. Prepare 1st draft on the New Bonus System. It should include:
        1. Purpose behind the change 
        2. Main principles of the new New Bonus System
        3. Example with “as is” and “to be” rewards for each lead
        4. Plan for New Bonus System implementation
    2. Feedback on the draft 
        1.  from Leads
        2.  from Councils
        3.  from JSG (from tomato?)
    3. Finalize New Bonus System based on the feedback
    4. Make the proposal & approve the proposal
    
    Additional
    
    - Understand how SCORES should be adjusted in order to cancel out all items that require input or feedback from the JSG