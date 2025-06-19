## Notebooks and chapter 
This documents contains the list of noteboks and chapters I already studied or are planning to study from this repository.

## Chapters
- [x] chap00
- [x] chap01
- [x] chap02
- [x] chap03
- [x] chap04
- [x] chap05
- [x] chap06
- [x] chap07
- [x] chap08
- [x] chap09
- [x] chap10
- [x] chap11
- [ ] chap12
- [ ] chap13
- [ ] chap14

## Examples
- [ ] Variability
- [ ] Temperature
- [ ] Ripoff_etf
- [ ] Resampling_animation

## tutorial
- [ ] time_series_01.ipynb
- [ ] time_series_02.ipynb
- [ ] time_series_03.ipynb

## Issues
1. sol/brfss.py -> update copyright year from 2010 to 2025
2. sol and nb/nsfg.py -> update copyright year from 2010 to 2025
3. sol and nb/populations.py -> update copyright year from 2015 to 2025
4. sol and nb/thinkstats.py -> update copyright year from 2024 to 2025
5. nb/thinkstats2.py -> update copyright year from 2024 to 2025
6. sol and nb/relay.py -> update copyright year from 2014 to 2025
7. nb/inc.py -> update copyright year from 2014 to 2025
8. tutorial/time_series_01/02/03.ipynb: copyright year from 2024 to 2025
9. Update copyright year in chapter notebooks from 2024 to 2025 (both sol and nb/chap01/2/3/4/5/6/7/8/9/10/11/12/13/14.ipynb)
10. Update copyright year in LICENSE from 2024 to 2025
11. Chapter 9: Hypothesis testing typo before title (hypothesis testing=)
12. Chapter 14: (chapter_analytic_methods)= text in the second cell before markdown title
13. Chapter 0: (section_nsfg)= Typo before the title "The National Survey of Family Growth"
14. Chapter 1: (section_summary_statistics)= Typo before "Summary statistics section"
15. Chapter 4: (section_comparing_cdfs)= Typo before "Comparing CDFs"
16. Chapter 5: (section_normal)= Typo before "The normal distribution"
17. Chapter 5: (section_lognormal_distribution)= typo before "The Lognormal Distribution"
18. Chapter 6: (section_exponential_pdf)= Typo before "The Exponential PDF"
19. Chapter 6: (section_kernel_density_estimation)= Typo before "Kernel Density Estimation"
20. chap8: (section_weighing_penguins)= Typo before "Weighing penguins"
21. Chap8: (section_estimating_variance)= Typo before "Estimating variance"
22. Chap8: (section_sampling_distributions)= Typo before "Sampling distributions"
23. Replaced ! in pip installs by % in all notebooks to install the python package in the correct environment
24. Chapter 1: plt is imported but not used
25. Chapter 1: "decorate" is imported but not used
26. Removed unnecessary pandas import from chapter 04
27. Chapter 5: plt is imported but not used
28. Chapter 5: multiple unnecessary redundant imports of empiricaldist
29. Unfilled placeholder "xxx" in nb and soln/chap03 "We'll revisit this question in Chapter xxx."
30. nb/soln/Chap07: typo -> "And here's what the distribution of GPAs looks like." But plots xlabel="Income (USD)"
31. nb/chapter02.ipynb -> last exercise solution -> rich group parity mean is lower than others parity mean but his answers
seems to explain why the rich group have more children than the others, when the effect size points otherwise.
32. Chapter 6: hardcoded mean of 2.2 (lam = 2.2) instead of lam = pmf_family.mean()
33. Chap08: exercise 8.5 -> For more on this problem, see [this Wikipedia page][https://en.wikipedia.org/wiki/German_tank_problem]
-> Parenthesis should be used in the link instead of brackets for correct markdown link display.
34. Chap09: "Next, we computed a **p-value**, which is the probability of seeing the observed effect if the null hypothesis is true.
P-value is the probability of observing an effect equal or bigger than the observed effect under the
null hypothesis, not the probability of observing an effect equal to the observed efffect.
35. Chap09: "So the hypothesis we'll test is whether pregnancy length is generally longer for first babies."
But uses abs value of the differences between groups "abs_diff_means" which is not computing whether pregnancy
length is generally longer for first babies but instead computes differences in both ways, longer or shorter
pregnancy lengths. So, most likely, the function should not be using abs value to avoid computing a two-sided
test but focus only on the cases where pregnancy length is longer for first than others. When a one sided test
is used, the p-value reduces to half from 0.18 to approximately 0.09. So, the conclusion holds but conceptually,
there is a discrepancy between what is being computed and what is said to be computed.
If we remove the abs fro abs_diff_means then it is necessary to adjust the make_pmf min value:
from `pmf = make_pmf(simulated_diffs, 0, 0.2)` to `pmf = make_pmf(simulated_diffs, -0.2, 0.2)` and the xlabel of the chart.
The same logic applies to "Other test statistics" on the same notebook on testing variation.
You might want to recycle some of your work on ElementsOfDataScience regarding Hypothesis testing on ThinkStats
chap09 as you have some great figures there and visual explanations help in understanting the topic.

### Unreported issues
None 

## Interesting python constructs
- chap03: pandas interval ranges as indices -> ranges = pd.interval_range(start=5, end=50, freq=5, closed="left")
- chap04: replacing values in a series -> birthwgt_lb.replace([51, 97, 98, 99], np.nan)
- chap05: from scipy.stats import trimboth -> trimmed = trimboth(birth_weights, 0.01) -> removing outliers
- chap06: np.allclose -> compare arrays element wise with a predefined tolerance
- chap07: pd.qcut(nlsy_valid["sat_verbal"], 10, labels=False) + 1 -> bin into deciles
- chap07: Series.quantile function to compute quantiles
- chap07: multiple subplots -> plt.subplot(2, 1, 1), plt.subplot(2, 1, 2); rows, columns
- chap07: plt.fill_between
- chap08: np.logspace -> generate an array of numbers spaced logarithmically
- chap08: weighted random sampling from a set of numbers: np.random.choice([1, 2.2], p=[0.98, 0.02], size=n)

## Ignore
I will skip the notebooks, chapters and examples not listed in this document.
