## Motivation: 
* Investigating on how hiring or ranking algorithms in general are biased and what are the effective ways to migating the bias.

## Background: 
* Exisiting hiring algorithms that companies claim to be "unbiased" oftentimes only try to avoid Equal Employment Opportunity Commission (EEOC) legal actions.
* Even when a hiring algorithm is "good enough", its interaction with human such as hiring manager still encourages discrimitory actions. 
* Two assessments of discrimination that would cause companies trouble: disparate treatment & disparate impact ("4/5" rule)
* Two general categories of current approaches to mitigating hiring algorithm: 
  * in-processing<sup>[1][2][3]</sup>: data cleaning -> ranking (normally done WIHTOUT machine learning)
  * post-processing<sup>[4][5][6]</sup>: data cleaning -> ranking -> evaluating -> reranking (normally done WITH machine learning, and evaluating and reranking could happen multiple times)
## Methodology: 

Experiemnt with a particular algorithm - Themis-ml (a fairness-aware post-processing machine learning algorihtm) by comparing the result of ranking with the result of final reranking. 
Evaluate both fairness and effectiveness by evaluating the mean difference between the binary group (protected and unprotected) and the AUC value.

## Main Finding:
before:
![image](https://user-images.githubusercontent.com/41777532/163516014-0076e8b5-1fe7-408b-b5e1-dece22c8c5ae.png)



## Evaluation:
Deploy real-life evaluation on the algorithm, e.g. hiring website like LinkedIn Tablent Search, to see if the algorithm achieves better marginalized group representation.

## Future Work / Next Steps: What you plan to do next / what remains to be done on your project.
* Explore the possibility to extend the algorithm so that it can support non-binary classification of groups. 
* werUnderstand the social and systemic dimension for hiring algorihtm to be in place.

## References: Citations for any prior work you referred to elsewhere on the poster.
[Fairness-Aware Ranking in Search & Recommendation Systems with Application to LinkedIn Talent Search](https://arxiv.org/abs/1905.01989)(Sahin Cem Geyik, Stuart Ambler, Krishnaram Kenthapadi)
[Mitigating Bias in Algorithmic Hiring: Evaluating Claims and Practices](https://dl.acm.org/doi/abs/10.1145/3351095.3372828) (Manish Raghavan, Solon Barocas, Jon Kleinberg, Karen Levy)
[Does Fair Ranking Improve Minority Outcomes? Understanding the Interplay of Human and Algorithmic Biases in Online Hiring](https://dl.acm.org/doi/abs/10.1145/3461702.3462602) (Tom Sühr, Sophie Hilgard, Himabindu Lakkaraju)
