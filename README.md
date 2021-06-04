**Background:**

The case was inspired by [Wikimedia Foundation Data Analyst Technical Assignment](https://github.com/wikimedia-research/Discovery-Hiring-Analyst-2016). The original dataset was transformed and adapted for the purposes of the workshop_. _

Discovery (and other teams within the Foundation) rely on event logging (EL) to track a variety of performance and usage metrics to help us make decisions. Specifically, Discovery is interested in:

**clickthrough rate:** the proportion of search sessions where the user clicked on one of the results displayed

**zero results rate:** the proportion of searches that yielded 0 results

and other metrics outside the scope of this task. EL uses JavaScript to asynchronously send messages (events) to our servers when the user has performed specific actions. In this task, you will analyse a subset of our event logs.

**Tasks:**

What is our daily overall clickthrough rate? How does it vary between the groups?

Which results do people tend to try first? How does it change day-to-day?

What is our daily overall zero results rate? How does it vary between the groups?

Let session length be approximately the time between the first event and the last event in a session. Choose a variable from the dataset and describe its relationship to session length. Visualize the relationship.

Summarize your findings in an executive summary.

**Basic Terms:**

**A/B Testing:**

A/B testing, at its most basic, is a way to compare two versions of something to figure out which performs better.

To run the test, you show two sets of users (assigned at random when they visit the site) the different versions (where the only thing different is the size of the button) and determine which influenced your success metric the most.

In real life there are lots of things that influence whether someone clicks. For example, it may be that those on a mobile device are more likely to click on a certain size button, while those on desktop are drawn to a different size. This is where randomization can help — and is critical. By randomizing which users are in which group, you minimize the chances that other factors, like mobile versus desktop, will drive your results on average.

**Observations:**

- During the AB test we have randomly split sessions into control group (old search) and treatment group (new search) and got to a 49.8% (old search) / 50.2% (new search) split. The test ran for 8 days, from March 1 till March 8th.
- Variation B&#39;s observed conversion rate (17.4%) was 74% lower than variation A&#39;s conversion rate (67%). The result is statistically significant.
- One potential reason for such a drop in CTR would be higher zero results rate in searches that were performed in group B sessions. However, this hypothesis was discarded as the difference in search results rate is not statistically significant.
- Session Lengths distribution also shows that Group B had shorter session lengths: 83% of sessions lasted less than 30s, while in Group A it was only 24%. Median session length for Group A was 111s, while for Group B it was 0s.

**A/B Test Outcome and Recommendation**

- Due to significant drop in Click Through Rate we should pause the A/B test immediately and revert to old search version. In the meantime, we should investigate what could have caused such a big drop.




