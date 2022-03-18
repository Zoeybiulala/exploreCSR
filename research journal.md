# ExploreCSR'22: Biased Hiring Algorithms

## Week 1: Feb 18 - Feb 25
- [x] Literature Review
1. [Mitigating Bias in Algorithmic Hiring: Evaluating Claims and Practices](https://dl.acm.org/doi/abs/10.1145/3351095.3372828) (Manish Raghavan, Solon Barocas, Jon Kleinberg, Karen Levy)

    * Main Takeaways: 
        * Uses [Crunchbase](https://www.crunchbase.com/) as data sourse; compares companies' claims and their practices
        * Two assessment of discrimination: disparate treatment & disparate impact("4/5" rule)
        * Findings: dispartiy between claims and actual hiring outcomes; to avoid litigation, companies do "within-group scoring" to control outcome to fit with 4/5 rules. 

2. [Does Fair Ranking Improve Minority Outcomes? Understanding the Interplay of Human and Algorithmic Biases in Online Hiring](https://dl.acm.org/doi/abs/10.1145/3461702.3462602) (Tom Sühr, Sophie Hilgard, Himabindu Lakkaraju)
 
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


3. [Algorithmic Equity in The Hiring of Underrepresented IT job Candidates](https://www.emerald.com/insight/content/doi/10.1108/OIR-10-2018-0334/full/html)(Lynette Yarger, Fay Cobb Payton, Bikalpa Neupane)
    * Main Takeaways:
        * Methodology: Feminist design and Theory by Costanza-Chock
        * types of bias (Chou et al.)
            * Data set bias
            * Association bias
            * Automation bias
            * Interaction bias
            * confirmation bias


4. [What You See Is What You Get? The Impact of Representation Criteria on Human Bias in Hiring](https://ojs.aaai.org/index.php/HCOMP/article/view/5281)(Andi Peng, Besmira Nushi, Emre Kıcıman, Kori Inkpen, Siddharth Suri, Ece Kamar)

    * Main Takeaways:
        * similar to #2: analyze the interplay of algorithms and human decisions
        * uses random profile generation as datasets; hiring participants to simulate online hiring process
        * How do personal features of the decision-maker, such as gender, impact the outcome? 



## Week2 Feb 26 - March 4
- [x] reach out to authors and ask about the datasets and algorithms
* post-processing algorithms:
   * [Det-Greedy](https://dl.acm.org/doi/pdf/10.1145/3292500.3330691?casa_token=OYEXJHAX7skAAAAA:60-IaTPwHoFaDMIPaGv7GIH7prytYtksqNHfFQ0rqE1hmGogQyscfQ1Vs6MykbqvDZE6QN9uNPau) Then they hand coded the algorithm based on the pesudocode (Tom Sühr)
   * [FA\*IR](https://github.com/fair-search) contains java and python version (Tom Sühr)
   * [elasticsearch](https://github.com/fair-search/fairsearch-fair-for-elasticsearch) (Tom Sühr)
   * [also elastic](https://milkalichtblau.github.io/pdf/zehlike_2021_fair_ranking_multiple_protected_groups.pdf) (Tom Sühr)
* in-processing algorithms:
   * [1](https://proceedings.neurips.cc/paper/2019/file/9e82757e9a1c12cb710ad680db11f6f1-Paper.pdf)(Tom Sühr)
   * [2](https://dl.acm.org/doi/pdf/10.1145/3219819.3220088?ref=https://githubhelp.com) (Karen Levy)
   * [3](https://www-ai.cs.tu-dortmund.de/LEHRE/SEMINARE/WS2021/TrustworthyAIMachineLearning/literature/yadav2019.pdfhttps://www-ai.cs.tu-dortmund.de/LEHRE/SEMINARE/WS2021/TrustworthyAIMachineLearning/literature/yadav2019.pdf)(Andi Peng)
* dataset:
   * [dataset for the fair algorith](https://github.com/MilkaLichtblau/FA-IR_Ranking/tree/FA-IR_CIKM_17)(Karen Levy)
   * [scraping from the web (applicants' info)](https://arxiv.org/abs/1901.09451) (Andi Peng)
   * [scraping from the web (job descripitons)](https://www.indeed.com/) (Anahita Samadi)

## Week3 March 5 - March 12
- [x] additional literature 
1. [RESUME RANKING USING MACHINE LEARNING — IMPLEMENTATION](https://medium.com/@Excellarate/resume-ranking-using-machine-learning-implementation-47959a4e5d8e) (Vinayak Joglekar)
   * An machine learning program that gives weighted scores to different attributes to a resume and decides if a resume is suitable.
   * Accuracy (compatibility of the program output and real hiring manager's decision) is gradually increasing when the data size is increasing.

2. [Attacks against Ranking Algorithms with Text Embeddings: a Case Study on Recruitment Algorithms](https://arxiv.org/abs/2108.05490) (Anahita Samadi, Debapriya Banerjee, Shirin Nilizadeh)
   * Main takeaways:
      * Because hiring ranking algorithm is based on text analysing, adversary could use certain text items to improve thier chances to get hired.
      * In a black box setting, one can use neural network based model to identify the most influential words without knowing the exact text embeding approach.
      * Two text embedding approaches: Universal Sentence Encoder (USE) and TF-IDF.


## Week4 March 13 - March 20
- [x] try out algorithms
   * [ranking with sat](https://github.com/MilkaLichtblau/FA-IR_Ranking/tree/FA-IR_CIKM_17)
      * Feldman ranking: determine protected group candidate *x*'s percentile within its group -> find the candidate *y* in un-protected group with the same percentile -> assign *y*'s score to *x*. 
      * Fair\*IR ranking: creates a ranked output that satisfies the fairness definition in :class:'FairnessInRankingsTester i.e. if all protected candidates already appear in the ranking the left over positions are filled with non-protected. 
      * *test-run*: showing fair ranking successful but stopped at feldman ranking - so no actual output showed up

   * [fair-search-java](https://github.com/fair-search/fairsearch-fair-java) 
      * important param:
         * k = total number of elements we need to rank
         * p = proportion of protected group in the top-k ranking
         * alpha = significance level (i don't understand)
      * comparing mtable generated by random ranking and re-rank the list by adjusting protected group's proportion in the top-k ranking.

   * [fair-search-python](https://github.com/fair-search/fairsearch-fair-python)
      * similar to java version


