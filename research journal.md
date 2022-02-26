# ExploreCSR'22: Biased Hiring Algorithms

## Week 1: Feb 18 - Feb 25
- [x] Literature Review
1. [Mitigating Bias in Algorithmic Hiring: Evaluating Claims and Practices](https://dl.acm.org/doi/abs/10.1145/3351095.3372828)

    * Main Takeaways: 
        * Uses [Crunchbase](https://www.crunchbase.com/) as data sourse; compares companies' claims and their practices
        * Two assessment of discrimination: disparate treatment & disparate impact("4/5" rule)
        * Findings: dispartiy between claims and actual hiring outcomes; to avoid litigation, companies do "within-group scoring" to control outcome to fit with 4/5 rules. 

2. [Does Fair Ranking Improve Minority Outcomes? Understanding the Interplay of Human and Algorithmic Biases in Online Hiring](https://dl.acm.org/doi/abs/10.1145/3461702.3462602)
    * Main Takeaways:
        * Uses Online hiring platforms (TaskRabbit) as data sourse; hires participants from Amazon Turk
        * ranking algorithm: FairDet-Greedy
        * asks how would inherent biases of employers interact with fair ranking algorithms and impact the real world hiring decisions?
        * Different notions of fairness have been proposed - but have not been validated in real world settings
            * *group fairness criterion*: propose post-processing approach to ensure underrepresented group has certain seats.
            * *individual equity-of-attention*: fairly divide attention between equally relevant candidates
        * Findings
            * fair ranking algorithms helped a little but the actual outcome still is influenced by employers' gender bias.
            * fair ranking algorithms is more effective when underrepresented candidate profiles are similar to those of the majority class
            * it became ineffective when employer choices already satisfy equal selection rates.


3. [Algorithmic Equity in The Hiring of Underrepresented IT job Candidates](https://www.emerald.com/insight/content/doi/10.1108/OIR-10-2018-0334/full/html)
    * Main Takeaways:
        * Methodology: Feminist design and Theory by Costanza-Chock
        * types of bias (Chou et al.)
            * Data set bias
            * Association bias
            * Automation bias
            * Interaction bias
            * confirmation bias


4. [What You See Is What You Get? The Impact of Representation Criteria on Human Bias in Hiring](https://ojs.aaai.org/index.php/HCOMP/article/view/5281)

    * Main Takeaways:
        * similar to #2: analyze the interplay of algorithms and human decisions
        * uses random profile generation as datasets; hiring participants to simulate online hiring process
        * How do personal features of the decision-maker, such as gender, impact the outcome? 



## Week2 Feb 26 - March 4
- [x] reach out to authors and ask about the datasets and algorithms (waiting for response)
* post-processing algorithms:
   * [Det-Greedy](https://dl.acm.org/doi/pdf/10.1145/3292500.3330691?casa_token=OYEXJHAX7skAAAAA:60-IaTPwHoFaDMIPaGv7GIH7prytYtksqNHfFQ0rqE1hmGogQyscfQ1Vs6MykbqvDZE6QN9uNPau) Then they hand coded the algorithm based on the pesudocode
   * [FA\*IR](https://github.com/fair-search) contains java and python version
   * [elasticsearch](https://github.com/fair-search/fairsearch-fair-for-elasticsearch)
   * [also elastic](https://milkalichtblau.github.io/pdf/zehlike_2021_fair_ranking_multiple_protected_groups.pdf)
* in-processing algorithms:
   * [1](https://proceedings.neurips.cc/paper/2019/file/9e82757e9a1c12cb710ad680db11f6f1-Paper.pdf)
   * [2](https://dl.acm.org/doi/pdf/10.1145/3219819.3220088?ref=https://githubhelp.com)
* dataset:
   * [dataset for the fair algorith](https://github.com/MilkaLichtblau/FA-IR_Ranking/tree/FA-IR_CIKM_17)
