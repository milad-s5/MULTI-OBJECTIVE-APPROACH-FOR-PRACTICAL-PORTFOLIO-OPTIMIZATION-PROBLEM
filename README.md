# A MULTI-OBJECTIVE APPROACH FOR PRACTICAL PORTFOLIO OPTIMIZATION PROBLEM
Repository for the convex optimization 2 course project:

- Milad Samimifar
---
For multi-objective portfolio optimization problems we use the mean-variance model as risk measures. Some of the evolutionary algorithms will solve all these portfolio optimization problems. In this project, we use NSGA-II and SMS-EMOA algorithms to solve the mean-variance model.

---
## MULTI OBJECTIVE OPTIMIZATION PROBLEM

A multi-objective portfolio optimization will optimize two objective
function, to minimize the risk and to maximize the return.
Hence the M-V model's multi objective problem is:

<p align="center">
<img width="400" alt="Screenshot 2022-10-07 105709" src="https://user-images.githubusercontent.com/82322980/201488420-880ad8c8-2975-45a2-8dca-1f27faa3596e.png">
</p>

## Data and code
We use daily profit of 24 shares at USA stock market(from NasdaqGS and NYSE with symbols 'SPY', 'FB', 'JCI', 'CMCSA', 'CPB', 'MO', 'MMC', 'JPM', 'ZION', 'PSA', 'BAX', 'BMY', 'LUV', 'PCAR', 'TXT', 'TMO', 'DE', 'MSFT', 'HPQ', 'SEE', 'VZ', 'CNP', 'NI', 'T') collected from Jan 2018 to Dec 2020 (Three years). We chose this interval so that the results are not affected by the effects of Corona. We used the two algorithms explained in the approach section and implemented them using Python code and received the outputs. You can see our notebook named `Project_codes.ipynb` in the attached files. For easier checking, this code has been converted into an .html file, which you can also view under the name `Project_codes.html`.

## Results
The first case Pareto optimal set of our data that we obtained with NSGA-II algorithm is plotted in Fig. 1.
The horizontal axis indicates expected return
and the vertical one is related to the risk.

<p align="center">
<img width="400" alt="Screenshot 2022-10-07 105709" src="https://user-images.githubusercontent.com/82322980/201490595-bc85906c-2543-43d5-b601-2d244e20c0e7.png">
</p>

And for the second case Pareto optimal set with SMS-EMOA algorithm is plotted in Fig. 2.

<p align="center">
<img width="400" alt="Screenshot 2022-10-07 105709" src="https://user-images.githubusercontent.com/82322980/201490655-2cc5d4c5-73e3-4dad-bb79-b2a2f7be93ef.png">
</p>

As you can see, both algorithms have reached almost the same set as output. But the first algorithm has more discontinuity in the obtained answers.

We took the risk rate as 0.02 and found the point with the highest Sharpe rate in Fig. 1 and Fig. 2. This point is a solution to the multi-objective problem, which is marked with a red cross in the figures. Now we can meaningfully compare the results of the algorithms, the obtained weights, etc.

<p align="center">
<img width="400" alt="Screenshot 2022-10-07 105709" src="https://user-images.githubusercontent.com/82322980/201490777-7433cd58-e975-49c7-ba4c-4ad756e449ed.png">
</p>

As can be seen from Table 1, both algorithms have assigned weights to similar symbols. The values assigned to the weights are slightly different, and the numbers are slightly changed every time the algorithm is executed. The reason is that the algorithms are evolutionary, so they do not reach a specific answer.

By comparing the two algorithms, it can be seen that in both algorithms, almost similar values of 0.42 for return and 0.23 for risk are obtained. On the other hand, the time to solve the problem by NSGA-II algorithm is equal to 18.7 seconds and 7.72 seconds for SMS-EOMA algorithm; so SMS-EMOA algorithm works almost twice better than NSGA-II algorithm in terms of execution time.

To check the output of the algorithms, we also made a comparison with equal weight values. As you can see in Table 2, in equal weights, the risks are almost equal with the two algorithms. But the final return is equal to 0.184, which shows that the two algorithms used have more than twice the performance improvement compared to the case of equal allocation of weights.



<p align="center">
<img width="400" alt="Screenshot 2022-10-07 105709" src="https://user-images.githubusercontent.com/82322980/201490861-6b4c21c8-8936-41c7-b515-90a5b4167bd1.png">
</p>

In Fig. 3, the final diagram of the weights in the two used algorithms is drawn.


<p align="center">
<img width="400" alt="Screenshot 2022-10-07 105709" src="https://user-images.githubusercontent.com/82322980/201490903-a12e1b4e-e02a-4d33-bb55-c82f37f0dda2.png">
</p>

## Conclusion
We could successfully form a two-objective portfolio
optimization problem to control return and risk. Also, we have carried out simulations some function of multi objective
portfolio optimization and each algorithm of NSGA-II and SMS-EMOA has been run. We then implemented and compared these algorithms. Our simulation
results for finding the global optimum of various functions suggest that both algorithms are same, but often SMS-EMOA algorithm
outperforms NSGA-II in terms time of execution. 

We also had an improvement on the mentioned algorithms by removing the weights that were less than a certain limit in each iteration of the evolutionary algorithms. This ultimately led to a decrease in the cardinality of the weights. 

