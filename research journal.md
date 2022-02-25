# ExploreCSR'22: Biased Hiring Algorithms

## Literature Review
1. [Mitigating Bias in Algorithmic Hiring: Evaluating Claims and Practices](https://dl.acm.org/doi/abs/10.1145/3351095.3372828)

* Hiring Models are inaccessible to the public & using their training data might jeopardize users' privacy.
* The only public data: companies' disclosure
* When relying on clients's *exisiting* employee's data (to perform the data validation or training), there is lack of data on those who *weren't* hired would have performed. 
> predicting the success of future employees based on current employees inherently skews the task toward finding candidates resembling those who have already been hired (p.474).
* Disparate Learning Processes (DLPs)

    #### When is an assessment considered discriminatory?
* disparate treatment: explictly treat candidates differently under Title VII
* disparate impact: "4/5" rule - the selection rate for one protected group is less than 4/5 of that of the group with the highest selection rate.
(but these are not the only indicators of bias.....)

    #### Methodologies
* data source: [Crunchbase](https://www.crunchbase.com/)  - start-up vendors' websites - disclosed information
* Documenting companies' claims and their practices

    #### Findings
* disparity between claims and actual outcomes
* facial analysis suffer from disparities in error rates across gender and racial lines (p.475).
* to avoid litigation, companies do "within-group scoring" to control outcome to fit with 4/5 rules. (how do you define the line that divides groups tho) (this might violet the disparate treatment..)

2. [Does Fair Ranking Improve Minority Outcomes? Understanding the Interplay of Human and Algorithmic Biases in Online Hiring](https://dl.acm.org/doi/abs/10.1145/3461702.3462602)

* Online hiring platforms
* Different notions of fairness have been proposed - but have not been validated in real world settings
    * *group fairness criterion*: propose post-processing approach to ensure underrepresented group has certain seats.
    * *individual equity-of-attention*: fairly divide attention between equally relevant candidates
* how would inherent biases of employers interact with fair ranking algorithms and impact the real world hiring decisions?

    #### Methodologies
* recruited 1079 participants to be proxy employers and used real world data from Taskrabbit
* proxy emplyers were given ranked candidates to hire for different tasks (**shopping, Event Staffing, and Moving Assistance**)
* algorithms:
    * *FairDet-Greedy*, *RabbitRanking*, *random ranking*
* analysis method: some regression model that I don't understand.. and Bonferroni correction; Wald test and Tukey's honest significant difference (HSD).

    #### Findings
* fair ranking algorithms helped a little but the actual outcome still is influenced by employers' gender bias.
* fair ranking algorithms is more effective when underrepresented candidate profiles are similar to those of the majority class
* it became ineffective when employer choices already satisfy equal selection rates.


3. [Algorithmic Equity in The Hiring of Underrepresented IT job Candidates](https://www.emerald.com/insight/content/doi/10.1108/OIR-10-2018-0334/full/html)

    #### Methodologies
* feminist design and theory by Costanza-Chock
    * Equity: Who gets to do design?
    * Beneficiaries: Who do we design for, or with?
    * Values: What values do we encode and reproduce in the objects and systems that we design?
    * Scope: How do we scope and frame design problems?
    * Sites: Where do we do design, what design sites are privileged, and what sites are ignored or marginalized, and how do we make design sites accessible to those who will be most impacted?
    * Ownership, accountability and political economy: Who owns and profits from design outcomes, what social relationships are reproduced by design, and how do we move toward community control of design processes?
    * Discourse: What stories do we tell about how things are designed?

* Some talent acquisition companies: 
    * Blendoor (removing identifying info from the resume);
    * GasJumpers(offers blind, skill-based test);
    * Interviewing.io(anonymous technical interview);
    * and Textio (write job advertisements that attract a diverse pool of applicants)

* types of bias (Chou et all.)
    * Data set bias
    * Association bias
    * Automation bias
    * Interaction bias
    * confirmation bias



    #### Findings
* algorithms may serve to codify deep-seated biases

4. [What You See Is What You Get? The Impact of Representation Criteria on Human Bias in Hiring](https://ojs.aaai.org/index.php/HCOMP/article/view/5281)

* kinda similar to #2: analyze the interplay of algorithms and human decisions

    #### research questions:

1. Doesbalancingthegenderdistributionincandidateslates mitigate bias? How does this effect vary across different professions?
2. In professions where this intervention is not enough, does over-representation help?
3. How do personal features of the decision-maker, such as gender, impact the outcome?

    #### methodology
* profile generation - HIT generation(similar to #2) - ranking task - statistical testing
