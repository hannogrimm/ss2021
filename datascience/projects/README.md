# Projects for Data Science
After my time with studying courses, I proceeded to get my hands on guided projects to practice. I chose DataCamp projects for this and one own project as a synthesis of all my learnings from the courses.

## Main Project: AMD & NVIDIA Stock Risk Comparison
[Click here to review the project.](self--stock-risk-comparison/archive/notebook.ipynb) My own project realizes the scenario of a friend that would like to make a single stock investment and is in need of a risk-comparison of two stocks. The target of this project is to implement my learnings of financial data analysis, risk management and data visualizations with `seaborn`. The steps of the project are expanded with self-written explanations and decorations to highlight my learnings.

## Guided Projects
The main emphasis of my guided projects was the handling and visualization of financial concepts. I oriented myself along the content of the courses I have taken on DataCamp. I saw the guided projects as an opportunity to put into practice what I have consumed through the courses. The projects have a focus on risk management and investment strategies.

As agreed with the module coordinator, two guided projects were found sufficient to apply the knowledge - with my main project (see above) serving as the third required project.

### Datacamp: Risk and Return - The Sharpe Ratio
This guided project introduced me to a new method of rating the value of return based on the implied risk of an investment. The Sharpe Ratio is a formula that can be applied to compare two assets on their risk-return ratio performance. The asset with the higher Sharpe Ratio provides a higher return for the same taken risk - and is therefore the favorable asset. The Sharpe Ratio was a relevant contribution to the Economic Nobel Prize of William F. Sharpe and is a common and relevant method to calculate return-per-risk still today. [Click here to review the project.](datacamp--risk-and-return-the-sharpe-ratio/notebook.ipynb)

### Datacamp: Which Debts are Worth the Bank's Effort?
This project does a statistical analysis on a potential _Regression Discontinuity_ in a bank's dataset of uncovered debts. The goal of the project is to review the case if the _actual recovery money_, i.e. the money _that can be_ paid back by the loantaker, reveals a significant jump after the threshold of 1000$ of _expected recovery money_ is met. The expected recovery money is measured by the banks through various (in this project unexplained) factors. Banks usually don't expect loans that cannot be covered by the loantaker anymore to be compensated with a relevant partial final pay-back (e.g. 50$ final compensation for 2000$ uncovered debt). To get the loantaker to send a partial final pay-back costs human resources. A pay-back of at least 50$ is therefore required to make the efforts "worth it". 

It is therefore to be analyzed if the hypothesis of a significant change in _actual recovery money_ occurs around the threshold of 1000$ of _expected recovery money_. Furthermore, it has to be made sure that the results are not influenced by other factors as age or sex of the loantaker. [Click here to review the project.](datacamp-which-debts-are-worth-the-banks-effort/notebook.ipynb)

### Reflection
I have found the two guided projects provided by DataCamp as insightful in their adressed topics, but found them to be a difficult source to learn further. Their approach of filling in the gaps is helpful to memorize the method names and common abbreviations for imported packages, but I am, based on my past experience of Software Engineering, convinced that the memorization of method names or arguments is not of dire importance and I will soon unmaster these again. I felt accomplished after finishing a project, but didn't feel a particular growth in my Data Science competencies. 

I therefore took the time to research and look further into the methods applicated, i.e. what should and can I do something with the `.agg` method of pandas DataFrames?

The projects were insightful regarding the financial education and I am happy I finished them. For example, the project on Sharpe Ratios gave me the insight into a common method to determine a simple risk-and-return comparison between two assets (i.e. is Facebook or Amazon a better investment at same risk?). This made me  curious to learn more about risk management and led me into starting a course on DataCamp on portfolio risk management in Python. I was able to utilize the projects as a great icebreaker into learning more of what I wanted to learn.

