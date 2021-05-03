# Projects for Data Science
Dated: Wed., 07. Apr 2021
Author: Hanno Grimm

## Main Project: AMD & NVIDIA Stock Risk Comparison
[Click here to review the project.](self--stock-risk-comparison/archive/notebook.ipynb) My own project realizes the scenario of a friend that would like to make a single stock investment and is in need of a risk-comparison of two stocks. The target of this project is to implement my learnings of financial data analysis, risk management and data visualizations with `seaborn`. The steps of the project are expanded with self-written explanations and decorations to highlight my learnings.

## Guided Projects
The main emphasis of my guided projects was the handling and visualization of financial concepts. I oriented myself along the content of the courses I have taken on DataCamp. I saw the guided projects as an opportunity to put into practice what I have consumed through the courses. The projects have a focus on risk management and investment strategies. 

### Datacamp: Risk and Return - The Sharpe Ratio
This guided project introduced me to a new method of rating the value of return based on the implied risk of an investment. The Sharpe Ratio is a formula that can be applied to compare two assets on their risk-return ratio performance. The asset with the higher Sharpe Ratio provides a higher return for the same taken risk - and is therefore the favorable asset. The Sharpe Ratio was a relevant contribution to the Economic Nobel Prize of William F. Sharpe and is a common and relevant method to calculate return-per-risk still today.

### Datacamp: Which Debts are Worth the Bank's Effort?
This project does a statistical analysis on a potential _Regression Discontinuity_ in a bank's dataset of uncovered debts. The goal of the project is to review the case if the _actual recovery money_, i.e. the money _that can be_ paid back by the loantaker, reveals a significant jump after the threshold of 1000$ of _expected recovery money_ is met. The expected recovery money is measured by the banks through various (in this project unexplained) factors. Banks usually don't expect loans that cannot be covered by the loantaker anymore to be compensated with a relevant partial final pay-back (e.g. 50$ final compensation for 2000$ uncovered debt). To get the loantaker to send a partial final pay-back costs human resources. A pay-back of at least 50$ is therefore required to make the efforts "worth it". 

It is therefore to be analyzed if the hypothesis of a significant change in _actual recovery money_ occurs around the threshold of 1000$ of _expected recovery money_. Furthermore, it has to be made sure that the results are not influenced by other factors as age or sex of the loantaker.
