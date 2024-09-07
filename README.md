**Experiment Overview: Free Trial Impact Study**

This project investigates a modification to Udacity’s free trial enrollment process. Currently, students can either "start a free trial" or "access course materials." Choosing the free trial requires entering credit card details, which results in enrollment in a paid course for 14 days. After this period, unless canceled, charges will be applied. Selecting "access course materials" allows free access to course content without coaching or certification.

In this experiment, Udacity introduced a new step: when opting for a free trial, students are asked about their weekly time commitment. Those indicating 5 or more hours per week proceed to checkout. If less than 5 hours, they are informed about the course’s typical time requirements and are offered the option to either proceed with the free trial or access course materials for free.

**1. Experiment Design**

**1.1 Unit of Diversion**

The unit of diversion is a cookie. Once a student enrolls in the free trial, they are tracked by their user ID. Each user ID can only enroll in the free trial once. For users who do not enroll, tracking does not continue beyond the course overview page visit.

**1.2 Initial Hypothesis**

The hypothesis is that this change will set clearer expectations for students, reducing the number of students who abandon the trial due to time constraints without significantly affecting the number of students who continue past the trial and complete the course. Successful results could enhance the student experience and optimize coaching resources.

**Initial Hypotheses:**

1. H0: The change does not affect the number of students who enroll in the free trial.

2. H1: The change reduces the number of students who enroll in the free trial.

3. H0: The change does not affect the number of students who abandon the free trial.

4. H1: The change reduces the number of students who abandon the free trial.

5. H0: The change does not affect the probability of students continuing the free trial beyond 14 days.

6. H1: The change increases the probability of students continuing the free trial beyond 14 days.

**1.3 Metric Choice**

Udacity’s metrics include:

1. Number of Cookies: Unique cookies viewing the course overview page (min = 3000)

2. Number of User IDs: Users enrolling in the free trial (min = 50)

3. Number of Clicks: Unique cookies clicking "Start free trial" (min = 240)

4. Click-Through Probability: Clicks divided by page views (min = 0.01)

5. Gross Conversion: Users completing checkout divided by clicks (min = 0.01)

6. Retention: Users remaining enrolled past 14 days divided by those completing checkout (min = 0.01)

7. Net Conversion: Users remaining enrolled past 14 days divided by clicks (min = 0.0075)

8. Invariant Metrics: Metrics expected to remain unchanged between the control and experimental groups, used for sanity checks:

9. Number of Cookies

10. Number of Clicks

11. Click-Through Probability

**Evaluation Metrics: **

Metrics used to assess the impact of the change:

Gross Conversion: Expected to decrease.

Retention: Expected to increase.

Net Conversion: Direction uncertain.

1.3.1 Hypothesis Revision

**Based on selected metrics:**

H0: Gross Conversion(control) = Gross Conversion(treatment)

H1: Gross Conversion(control) ≠ Gross Conversion(treatment)

H0: Retention(control) = Retention(treatment)

H1: Retention(control) ≠ Retention(treatment)

H0: Net Conversion(control) = Net Conversion(treatment)

H1: Net Conversion(control) ≠ Net Conversion(treatment)

**2. Measuring Standard Deviation**

In binomial distribution, standard deviation = sqrt(p(1-p)/n).

Standard Deviation for Evaluation Metrics:

Gross Conversion: 0.0202

Retention: 0.0549

Net Conversion: 0.0156

**3. Sizing**

With alpha set to 0.05 and beta to 0.20, sample sizes needed are:

Gross Conversion: 645,875

Retention: 4,741,212

Net Conversion: 685,325

To test hypotheses, 4,741,212 pageviews are required.

**3.0.1 Multiple Hypothesis Testing**

Given the interdependence of hypotheses, we chose not to apply Bonferroni Correction to avoid increasing false negatives.

**3.1 Choosing Duration vs. Exposure**

Considering a daily traffic of 40,000 pageviews:

For gross conversion, retention, and net conversion: 119 days are required.

For gross and net conversion: 17 days are required.

Opting to exclude the retention metric, the experiment duration for gross and net conversion is:

50% traffic: 34 days

45% traffic: 38 days

Decision: Use 50% traffic for 34 days.


**4. Experiment Analysis**

**4.1 Sanity Check**

4.1.1 Visualization Visualization of invariant metrics shows consistency across control and experimental groups.

4.1.2 Statistical Checks

Cookies, Clicks, and Click-Through Probability fall within expected ranges.

**4.2 Result Analysis**

4.2.1 Visualization Visual comparison of evaluation metrics between control and experimental groups.

4.2.2 Statistical and Practical Significance

Gross Conversion: Decreased by 2.06%, statistically and practically significant.

Net Conversion: Slight decrease of 0.49%, not significant.

4.2.3 Weekly Analysis

Gross conversion is less effective on Thursdays.

Net conversion shows more fluctuation, with Wednesday and Sunday being less effective.

**4.3 Results Interpretation & Recommendations**

Gross Conversion: A significant decrease indicates that the change filters out less committed users but may negatively impact the overall enrollment rate.

Net Conversion: Not significantly affected, suggesting that while the trial enrollment may decrease, it does not translate to better payment conversion.

Recommendation: Given the significant impact on gross conversion but not on net conversion, consider further experiments to refine the process or explore alternative strategies.

**5. Follow-Up Experiment: Reducing Early Cancellations**
   
Pre-Enrollment: Enhance the time commitment form to include prerequisites and offer a clear path to access free materials for less committed users.

Post-Enrollment: Implement a peer group system to increase engagement and retention.

Experiment Design: Randomly assign enrolled students to control or experimental groups with group assignments led by mentors.

Unit of Diversion: User-IDs.

**Hypothesis:**

H0: Group assignments do not significantly increase retention after the 14-day free trial.
H1: Group assignments significantly increase retention after the 14-day free trial.
Invariant Metrics: Number of User IDs.

Evaluation Metric: Retention rate.

If significant positive changes are observed, and resources are acceptable, proceed with the experiment.
