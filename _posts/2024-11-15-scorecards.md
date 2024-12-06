# The Art and Science of Credit Risk Scorecards
## Planning


```python

```

### 1. Overview

Increased competition and growing pressures for revenue generation have led credit-granting and other financial institutions to search for more effective ways to attract new creditworthy customers, and at the same time, control losses

Aggressive marketing efforts have resulted in deeper penetration of the risk pool of potential customers, and the need to process them rapidly and effectively has led to growing automation of the credit and insurance application and adjudication processes.

Customer service excellence demands that this automated process be able to minimize denial of credit to creditworthy customers, while keeping out as many potentially delinquent ones as possible.

At the customer management level, companies are striving ever harder to keep their existing clients by offering them additional products and enhanced services:
- Offer favored treatment for good customers (i.e., low risk)
- Devise strategies to not only identify bad customers (non-payment, fraud), but also deal with them effectively to minimize further loss and recoup monies owed, as quickly as possible.

In such environment, risk scorecards offer a powerful, empirically derived solution to business needs. Risk scorecards have been used by a variety of industries for uses including predicting delinquency nonpayment—that is, bankruptcy—fraud, claims (for insurance), and recovery of amounts owed for accounts in collections. Scoring methodology offers ***an objective way to assess risk***, and also ***a consistent approach***, provided that system overrides are kept to a minimum.

### 2. Process

The process of scorecard development needs to be a collaborative one between information technology (IT), data mining, and operational staff. This not only creates better scorecards, it ensures that the solutions are consistent with business direction, and enables education and knowledge transfer during the development process.

Involving these resources in the scorecard development and implementation project helps to incorporate collective organizational knowledge and experience and produces scorecards that are more likely to fulfill business requirements

The following list describes the ideal checklist of stages and tasks to develop a scorecard. Details of some key stages are described in sections that follow.

*STAGE 1. PRELIMINARIES AND PLANNING*
- Create business plan
- Identify organizational objectives and scorecard role
- Determine internal versus external development and scorecard type
- Create project plan
- Identify project risks
- Identify project team and responsibilities

<a href="### 3. Data Review and Project Parameters">*STAGE 2. DATA REVIEW AND PROJECT PARAMETERS*</a>
- Data availability and quality
- Data gathering for definition of project parameters
- Definition of project parameters
- Performance window and sample window
- Performance categories definition (target)
- Exclusions
- Segmentation
- Methodology
- Review of implementation plan

*STAGE 3. DEVELOPMENT DATABASE CREATION*
- Development sample specifications
- Sampling
- Development data collection and construction
- Adjustment for prior probabilities (factoring)

*STAGE 4. SCORECARD DEVELOPMENT*
- Exploring data
- Identifying missing values and outliers
- Correlation
- Initial characteristic analysis
- Preliminary scorecard
- Reject inference
- Final scorecard production
- Scorecard scaling
- Choosing a scorecard
- Validation

*STAGE 5. SCORECARD MANAGEMENT REPORTS*
- Gains tables
- Characteristic reports

*STAGE 6. SCORECARD IMPLEMENTATION*
- Preimplementation validation
- Strategy development
    - Scoring strategy
    - Setting cutoffs
    - Policy rules
    - Overrides

*STAGE 7. POSTIMPLEMENTATION*
- Scorecard and portfolio monitoring reports
    - Scorecard management reports
    - Portfolio performance report

### 3. Data Review and Project Parameters

It is designed to determine whether scorecard development is feasible and to set high-level parameters for the project.

The parameters include: ***exclusions***, ***target definition***, ***sample window***, and ***performance window***.

#### Data Availability and Quality

This phase first addresses the issue of data availability, in the contexts of ***quality*** and ***quantity***. \
***Reliable and clean data*** is needed for scorecard development, with ***a minimum acceptable number of "goods" and "bads"***.

The quantity of data needed varies, but in general, it should fulfill the requirements of statistical significance and randomness. Exact numbers are not critical, since that depends upon the "bad" definition to be set in the next phase. However, as a rule of thumb: \
\-  For ***application scorecard*** development there should be approximately 2,000 “bad” accounts and 2,000 “good” accounts that can be randomly selected for each proposed scorecard, from a group of approved accounts opened within a defined time frame. \
\- For ***behavior scorecards***, these would be from a group of accounts that were current at a given point in time. \
\- For ***collections scoring***, these would be at a certain delinquency status. \
\- A further 2,000 ***declined applications*** may also be required for application scorecards where ***reject inference*** is to be performed. \
*Typically, it is more difficult to find enough “bad” accounts than “good” ones.*

Once it is determined that there is sufficient good-quality internal data to proceed, external data needs must be evaluated, quantified, and defined. The organization may decide to develop scorecards based on internal data alone, or may choose to supplement this data from external sources such as credit bureaus, central claims repositories, geo-demographic data providers, and so forth. \
Some organizations obtain and retain such data for each applicant in electronic databases. In cases where data is not available electronically, or is retained in paper-based format, the organization may have to either key it into databases or purchase data on a “retroactive” basis from the external provider. The timeframe for “retro” data extracts is specified in line with the performance and sample window definitions to be specified.

***When it is determined that both quality and quantity of internal and external data can be obtained, the initial data gathering for project parameters definition can begin***

#### Data Gathering for Definition of Project Parameters

Data must first be gathered in a database format to define project parameters which primarily include: \
\- determining the definitions of "good" and "bad", \
\- establishing the performance and sample windows, \
\- defining data exclusions for use in producing the development sample and in the development process itself.

***For applications***,  data items are usually collected from the previous two to five years, or from a large enough sample. \
***For behavior scorecard*** development, accounts are chosen at one point in time, and their behavior analyzed over, typically, a 6- or 12 month period.

#### Definition of Project Parameters

##### Exclusions

Certain types of accounts need to be excluded from the development sample. In general, accounts used for development are those that you would score during normal day-to-day credit-granting operations, and those that would constitute your intended customer.

Accounts that have abnormal performance - for example, frauds—and those that are adjudicated using some non-score-dependent criteria should not be part of any development sample. These can include designated accounts such as staff, VIPs, out of country, preapproved, lost/stolen cards, deceased, underage, and voluntary cancellations within the performance window

If there are geographic areas or markets where the company no longer operates, data from these markets should also be excluded so that the development data represents future expected status. For example, an auto loan company used to provide financing for the purchase of recreational vehicles such as snowmobiles, watercrafts, and all-terrain vehicles (ATV). However, a year ago it decided to focus on its core personal auto financing business, and stopped financing all other assets. For scorecard development purposes, the development data for this company should only include loan applications for personal autos.

In general, a way to look at ***exclusions*** is to consider it as a ***sample bias*** issue.

 ##### Performance and Sample Windows and “Bad” Definition

 ***"Future performance will reflect past performance."*** is the assumption used in scorecard development. \
 Based on this assumption, the performance of previously opened accounts is analyzed in order to predict the performance of future accounts.

In order to perform this analysis, we need to gather data for accounts opened during a specific time frame, and then monitor their performance for another specific length of time to determine if they were good or bad. The data collected (the variables) along with good/bad classification (the target) constitutes the development sample from which the scorecard is developed.

- ***"Performance Window"*** is the time window where the performance of accounts opened during a particular time frame (i.e., the sample window) is monitored to assign class (good/bad).
- ***"Sample Window"*** refers to the time frame from which known good and bad cases will be selected for the development sample. \

*In some cases, such as fraud and bankruptcy, the performance class is already known or predetermined. It is still useful, however, to perform the analysis described next, in order to determine the ideal performance window.*

A simple way to establish performance and sample windows is to analyze payment or delinquency performance of the portfolio, and plot the development of defined “bad” cases over time. A good source of this data is the monthly or quarterly cohort or vintage analysis report

**Vintage/cohort analysis**

An example of a vintage/cohort analysis, for a “bad” definition of 90 days delinquent and a 9-month performance window, is shown as below:
![image.png](attachment:dc8dbaff-8eac-4c2c-bcd4-651026b67693.png) \
The figures highlighted (showing current delinquency status by time on books for accounts opened at different dates) are plotted for this analysis.
The figures refer to the proportion of accounts delinquent after certain months as customers. For example, in the first line, 2.4% of accounts opened in January 2003 were 90 days past due after five months as customers.

The below plot of bad rate by month opened (tenure) for a 14-month period.
![image.png](attachment:68952e02-c15b-481b-b5b1-06c6685f7c77.png) \
This exhibit shows an example from a typical credit card portfolio where the bad rate has been plotted for accounts opened in a 14-month period. It shows the bad rate developing rapidly in the first few months and then stabilizing as the account age nears 12 months.

Selecting development samples from a mature cohort is done to minimize the chances of misclassifying performance (i.e., all accounts have been given enough time to go bad) and to ensure that the “bad” definition resulting from an immature sample will not understate the final expected bad rates.

 ***The time taken for accounts to mature varies by product and by "bad" definition selected.***

***Behavior scorecards*** for operational use are typically built for performance windows of ***6 or 12 months***. ***Collections models*** are typically built for performance windows of ***one month***, but increasingly, financial companies are building such scorecards for ***shorter windows of up to two weeks***, to facilitate the development of more timely collection path treatments. 


***When developing predictive models for specific regulatory requirements—for example, the Basel II Accord—the performance window may be dictated by the regulation.***

This analysis should be repeated for several relevant delinquency definitions. This is done because the different definitions will produce differing sample counts. \
In cases of bankruptcy or chargeoff scorecards, only one analysis is sufficient since there is only one possible definition of "bad".

Where possible, this analysis should be done using the "ever bad" definition.If this is not possible, normally due to data difficulties, then a "current" definition of "bad" will suffice, where the delinquency status of accounts is taken from the most recent end-of-month performance.

 ##### Effect of Seasonality

The variation of application and approval rates across time, and the effect of any seasonality, should also be established at this point. \
***The development sample*** (from the sample window) must be ensured not to include any data from "abnormal" periods, so that the sample used for development is in line with normal business periods, representing ***the typical "through the door" population***.

The objective here is to conform to the assumption that ***"the future is like the past"***. In practical terms, this helps to generate ***accurate approval rate/bad rate predictions***, and more importantly, produces scorecards that will be ***robust*** and ***stand the test of time***.

In reality, ***such exercises are done*** largely to catch extreme behavior, since ***establishing a standard for “normal” is difficult***. There are several ways to counter the effects of abnormal periods when the applicant population does not represent the normal "through the door" population.
- This is best done through analysis comparing the characteristics of the average customer with the characteristics of those from the sample window.
- Further reasons for profile shifts can also be gleaned from information on marketing campaigns active during the sample window, or any other factor that can affect the profile of credit applicants.

**Example:**
An organization expects credit card applicants to be ***mostly mature men and women***, but discovers that the applicants from its desired one-month sample window are ***mostly young men***. \
<u>***Reason:***</u> An analysis of marketing campaigns shows that the company was actively pursuing applications at a booth in an auto show during that month (auto shows typically attract young men as customers). \
<u>***Solution:***</u> \
\- Equipped with this information, the company can then ***expand the sample window*** to three or more months long, to smooth out the effects of that particular month. \
\- Another technique to "normalize" data is to ***filter out the source of abnormality***. if the company is certain that it will not target young males in the future, and that the performance of these young males will distort their overall expected portfolio, then ***the company may choose to exclude young males from its development sample***.

 
    

 ##### Definition of "Bad"

The purpose of this phase is to categorize account performance into 3 primary groups:
- "bad"
- "good"
- "indeterminate"

For cases of brankruptcy, chargeoff, or fraud, the definition of "bad" is fairly straightforward. \
For contractual-deliquency-based definition, there are many choices based on levels of delinquency. For different definitions of "bad", it will produce a different sample count for "bad" accounts. \
In general, the definition of what constitutes a “bad” account relies on several considerations:
-  The definition must be <u>in line with organizational objectives</u>. If the objective is to increase profitability, then the definition must be set at a delinquency point where the account becomes unprofitable. This can get complicated where accounts that are, for example, chronically paying late by a month but do not roll forward to two or three months may be profitable. <u>For insurance applications</u>, a dollar value on claims may be appropriate. <u>If delinquency detection is the objective</u>, the definition will be simpler
 (e.g., “ever” 60 or 90 days).
- The definition must be <u>in line with the product or purpose</u> for which the scorecard is being built. <u>For example</u>, bankruptcy, fraud, claims (claim over $1,000), and collections (less than 50% recovered within three months).
- <u>A “tighter,” more stringent definition</u> - for example, "write-off" or "120 days delinquent" - provides a more extreme (and precise) differentiation, but in some cases, may yield low sample sizes.
- <u>A “looser” definition</u> (e.g., 30 days delinquent) will yield a higher number of accounts for the sample, but may not be a good enough differentiator between good and bad accounts, and will thus produce a weak scorecard.
- The definition must be <u>easily interpretable and trackable</u> (e.g., ever 90 days delinquent, bankrupt, confirmed fraud, claim over \$1,000). <u>Choosing a simpler definition</u> also makes for easier management, and decision making - any bad rate numbers reported will be easily understood.
- The definitions may be selected based on <u>accounting policies on write-offs</u>.
-  In some cases, it may be beneficial to have <u>consistent definitions of "bad"</u> across various segments and other scorecards in use. This makes for easier management and decision making, especially in environments where <u>many scorecards are used</u>. Coupled with consistent scaling of scores, this also <u>reduces training and programming costs when redeveloping scorecards</u>.
- <u>Regulatory or other external requirements may govern how delinquency is defined</u> (distinct from the organization’s own operational definition).Regulatory reporting requirements for the new Basel II Capital Accord is an example of this - "bad" definitions in the future may be required to be linked to economic loss, a specific default level, or a particular level of expected loss. <u>Based on the new Basel II Capital Accord, the definition of default is generally 90 days delinquent</u>.
- *In some cases, "bad" definitions are <u>chosen by default, due to a lack of data or history</u>. <u>For example</u>, an organization only kept records for a 12-month history, the only "bad" definition that showed maturity during analysis was "ever 30 day". Or, some organizations do not keep monthly payment data, and the only option for defining "bad" is current delinquency status (compared to "ever").*

 ##### Confirming the "Bad" definition

Once an initial "bad" definition is identified using the analysis and arguments above. Further analysis can be done to confirm it, to make sure
that those identified are indeed truly bad. The confirmation can be done using <u>expert judgment</u>, <u>analysis</u>, or <u>a combination of both</u>, depending on the resources and data available.

**Consensus method** \
<u>The judgmental or consensus method</u> involves <u>various stakeholders</u> from Risk, Marketing, and Operational areas getting together and reaching a consensus on the best definition of a "bad" account, based on <u>experience</u> and <u>operational considerations</u>, as well as the analysis covered above

**Analytical Methods** / 
Two analytical methods to confirm "bad" definitions will be commonly taken:
1. Roll rate analysis
2. Current vs. worst delinquency comparison

*In addition to these two, profitability analysis can also be performed to confirm that those defined as bad are unprofitable, or produce negative net present value (NPV). While this can be done <u>easily at monolines</u> (e.g., retail card providers), it is <u>not an easy task at multiproduct environments</u> such as banks*

- **Roll rate analysis**: Roll rate analysis involves comparing worst delinquency in a specified "previous x" months with that in the "next x" months, and then <u>calculating the percentage of accounts</u> that <u>maintain their worst delinquency</u>, <u>get better</u>, or <u>"roll forward" into the next delinquency buckets</u>. \
The purpose here is <u>to identify a "point of no return"</u> (i.e., the level of delinquency at which most accounts become incurable).\
\
***Deliquency history for an account*** \
![image.png](attachment:87b8e753-ac12-4ffb-bca3-99b24e40dacc.png) \
***Roll rate chart*** \
![image.png](attachment:42810aad-d505-4ef4-b017-32eb08ab59a6.png) \
<u>In the above example</u>, only about <u>18% of accounts that were ever 30 days delinquent</u> in the previous 12 months <u>rolled forward to being 60 and 90+ days delinquent</u>, but <u>almost 70% of accounts that reach 90-day delinquency roll forward to worse delinquency</u>. In this case, the “ever 90 days delinquent” definition of "bad" makes more sense, as it truly isolates those that remain delinquent. Conversely, the 30-day “bad” definition will be inappropriate, since most of those accounts roll back (cure) to being current. \
Inconclusive evidence in this analysis may point to potential “indeterminate” status. \
*It is <u>worth noting</u> that <u>the Basel II Capital Accord</u> defines <u>"default"</u> as <u>any point at which the bank considers the obligor unlikely to repay the debt in full</u>, and <u>specifies 90 days past due as a definition</u>.*

- **Current versus Worst Delinquency Comparison**: This method is <u>similar in concept</u> to the roll rate analysis, but is <u>simpler to execute</u>. It compares <u>the worst (ever) delinquency status</u> of accounts with their <u>most current delinquency</u> status. \
As with roll rate analysis, the objective here is also to <u>look for a "point of no return"</u>.\
\
**Comparing ever to current delinquency** \
![image.png](attachment:7b2d3627-b5a5-4602-89e7-0a35245a4c8b.png) \
The example shows that out of all accounts that ever go to 30 day delinquency, a vast majority - 84% - have no delinquency at present. In contrast, 60% of all accounts that go to 90-day delinquency stay at 90 days or become worse. This again confirms that a 90- or 120- day definition of "bad" is an adequate one.\
*It should be noted that <u>the preceding analyses to determine and confirm "bad" definitions</u> could be performed for <u>both application</u> and <u>behavior scorecards</u>. Even though behavior scorecards are usually developed to predict over a six-month window, it is still useful to perform this analysis to determine "bad" definitions.*

 ##### "Good" vs. "Indeterminate"

Again, defining "good" must be <u>in line with organizational objectives</u> and <u>other issues discussed earlier</u>. Defining "good" accounts is <u>less analytical, and usually obvious</u>. Some characteristics of a good account that should be kept in mind for consideration:
- <u>Never delinquent</u> or <u>delinquent to a point where forward roll rate is less than, for example, 10% </u>.
- <u>Profitable</u>, or <u>positive NPV</u>.
- No claims
- Never bankrupt
- No fraud
- Recovery rate of, e.g., 50% in collections.
    
A point to note is that, while <u>good accounts need to retain their status over the entire performance window</u>, <u>a bad account can be defined by reaching the specified delinquency stage at any time in the performance window</u> (*as per the “ever” definition*). \
\
Thus, indeterminate accounts are those that do not <u>conclusively fall into either the "good" or "bad" categories</u>. These are accounts that 
- <u>do not have sufficient performance history for classification</u>, or 
- that have some mild delinquency with roll rates *neither* <u>low enough to be classified as good</u>, *nor* <u>high enough to be bad</u>.
    
For example, indeterminate can include:
- Accounts that hit 30- or 60-day delinquency but do not roll forward (i.e., are not conclusively bad);
- Inactive and voluntarily canceled accounts, "offer declined" accounts, applications;
- Accounts with insufficient usage - for example, credit card accounts with a "high balance" of less than $20;
- Insurance accounts with claims under a specified dollar value;
- Accounts with NPV = 0.

*<u>Note that:</u>*
-  All canceled and "not taken up" accounts are sometimes assigned as rejects, or excluded, assuming that they were likely not their intended customers. However, <u>accounts that cancel voluntarily are your intended customers</u> and <u>may have canceled due to customer service issues</u>.  If they reapplied, they would <u>be rescored and likely approved again</u>. Therefore, these <u>should be included in the scorecard development process as indeterminate</u>.
-  <u>Indeterminates are only used</u> where <u>the "bad” definition" can be established several ways</u>, and are usually not required where the definition is clear-cut (e.g., bankrupt). As a rule of thumb, indeterminates <u>should not exceed more than 10% to 15% of the portfolio</u>.
    -  In cases where the proportion of indeterminates is very high (e.g., where a large portion of inactive accounts is present), analyses should be done to address root causes of inactivity - e.g. presence of other cards with higher limits or lower interest rates, presence of other cards with better loyalty programs, or inactivity with all other cards as well
- <u>Only accounts defined as "good" and "bad" (and rejects for application scorecard)</u> are <u>used in the actual development</u> of the scorecard. <u>Indeterminates are added</u> when forecasting to <u>adequately reflect the true “through the door” population</u>, since these are applicants who will be scored and adjudicated, and therefore <u>all approval rate expectations must reflect their presence</u>.
- In cases such as <u>application scorecards</u>, where ***reject inference is to be used***, <u>an additional performance category needs to be included in the development sample for “declined” applications</u> (i.e., those who were declined credit or services). This enables a development sample to be created that <u>reflects the performance of the entire applicant population</u>, and not just that of the approved.

#### Segmentation

In some cases, using <u>several scorecards</u> for a portfolio provides ***better risk differentiation*** than using <u>one scorecard</u> on everyone.  This is usually the case where
- A population is made up of <u>distinct subpopulations</u>;
- One scorecard will not work efficiently for all of them, assuming that <u>different characteristics</u> are required to predict risk for <u>the different subpopulations</u> in our portfolio.

=> Identifying these subpopulations, called ***segmentation***. 02 main ways in which ***segmentation*** can be done:
1. Generating <u>segmentation ideas based on experience and industry knowledge</u>, and then <u>validating these ideas using analytics</u>.
2. Generating <u>unique segments using statistical techniques</u> such as clustering or decision trees.

*<u>Note that:</u>*
- Any segments selected <u>should be large enough</u> to enable meaningful sampling for separate scorecard development.
- ***A "distinct" population*** is <u>not recognized as such based only on its defining characteristics (such as demographics)</u> (*risk profile*), but rather on <u>its performance</u> (*risk-based performance*).
- ***Detecting different behavior*** on its own is, however, <u>not a sufficient reason</u> for segmentation, the difference needs to <u>translate into measurable effects on business</u> (e.g., lower losses, higher approval rates for that segment). How to measure this is given in the ***"Comparing Improvement"***.
- Segmentation, whether using experience or statistical methods, should also be done with future plans in mind. <u>Most analysis and experience is
 based on the past</u>, but <u>scorecards need to be implemented in the future</u>, on <u>future applicant segments</u>.
 
*The Basel II Capital Accord takes <u>a pragmatic view of segmentation</u> by defining segments as ***"homogenous risk pools"***. This leaves individual banks across the world with the option of <u>defining their own unique segments<u>, <u>without a prescriptive recipe for everyone</u>.*

**Experience-Based (Heuristic) Segmentation** \
Segmentation ideas are generated from <u>business knowledge and experience</u>, <u>operational considerations</u>, and <u>industry practices</u>.
 
Once ideas on segmentation are generated, further analysis needs to be done for two reasons:
1. These ideas need to <u>be confirmed with at least some empirical evidence</u> to provide a comfort level.
2. Analysis can help in <u>better defining segments</u> such as thin/thick file, postal code groups, and young/old age, by <u>suggesting appropriate breakpoints</u>.

Some methods may be used:
- <u>One simple method</u> to <u>confirm segmentation ideas</u> and to <u>establish the need for segmentation</u> is to <u>analyze the risk behavior of the same characteristic</u> across <u>different predefined segments</u>.
- Another way to confirm initial segmentation ideas, and to identify unique segments, is to <u>look at observed bad rates for different selected subpopulations</u>.

*Both the methods described above are fairly simple to implement, and can provide some measure of comfort that the segments chosenthrough experience and intuition are appropriate*.

**Statistically-Based Segmentation** \
**Clustering** is a widely used technique to <u>identify groups that are similar to each other with respect to the input variables</u>. The objects in each cluster tend to be similar to each other in some sense, and objects in different clusters tend to be dissimilar. Two of the methods used to form clusters are:
- K-meansclustering, and 
- Self-organizing maps (SOMs)

*Noted that clustering identifies groups that are <u>similar based on their characteristics - not performance</u>. Thus, clusters may seem to be different, but may have similar risk performance. <u>The clusters therefore should be analyzed further</u>, using, for example, <u>bad rate analysis</u>, to ensure that the <u>segmentation produced</u> is for <u>groups with different risk performance</u> profiles.*

**Decision trees** isolate segments based on performance criteria (i.e., differentiate between "good" and "bad"). Decision trees not only identify characteristics for segmentation, but also identify optimum breakpoints for each characteristic. Thus representing a very powerful and convenient method for segmenting. The below example shows segmentation based on two levels with the result of four possible segments for this port
folio, based on existing/new customer, length of tenure, and age. \
![image.png](attachment:75f5cd82-6d87-4dba-9fd7-b093007413cc.png)

**Comparing Improvement** \
Both experience-based and statistical analyses will <u>yield ideas for potential segmentation</u>, and may <u>confirm that there are sufficient reasons for segmenting</u> - but they ***do not quantify the benefits of segmenting***. /
There are fairly simple ways available to estimate whether the improvement through segmentation is worth pursuing. /
1. The first step is to measure the improvement in predictive power through segmentation. This can be done using a number of statistics such as the Kolmogorov-Smirnov (KS), c-statistic, and so on. \
***Comparing improvements through segmentation***
![image.png](attachment:367490ac-57ff-4051-82e2-d5c4588a1949.png) \
The user then needs to decide what level of improvement is significant enough to warrant the extra development and implementation effort. That question is best answered using ***business, not statistical, measures***. Businesses are not run to maximize c-statistics or KS - they are run based on ***performance indicators such as approval rates, profits, loss rates, and so forth***. It would therefore be useful to <u>convert improved predictive power into expected portfolio performance</u> and here is the example: \
***Gauging business benefit of Segmentation*** \
![image.png](attachment:9b72da60-75e5-4902-b22c-ca1b2119a929.png) \
The exhibit compares two common performance measures, namely <u>the approval rate</u> and <u>expected bad rate</u>, for each segmented scorecard. It also lists <u>the approximate size of each segment</u>. Using these metrics can help decide if the combination of the size of the segment and the improvement in performance is enough to justify additional scorecard implementation.

**Choosing segments** \
There are many factors to consider in implementing scorecards, including:
- Cost of Development
- Cost of Implementation
- Processing
- Strategy Development and Monitoring

#### Methodology

There are various mathematical techniques available to build risk prediction scorecards. The most appropriate technique to be used can depend on issues such as:
- The quality of data available.
- Type of target outcome, that is, binary (good/bad) or continuous($ profit/loss).
- Sample sizes available.
- Implementation platforms.
- Interpretability of results.
- Legal compliance on methodology.
- Ability to track and diagnose scorecard performance.

At this point, the scaling and structure of the scorecard can also be discussed:
- The potential score ranges, 
- Points to double the odds, if the score itself represents the expected bad rate, 
- etc.
