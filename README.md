# 2024-2025 Multi order stochastic temporal injection using Tenet framework

Optional project of the [Streaming Data Analytics](https://emanueledellavalle.org/teaching/streaming-data-analytics-2024-25/) course provided by [Politecnico di Milano](https://www11.ceda.polimi.it/schedaincarico/schedaincarico/controller/scheda_pubblica/SchedaPublic.do?&evn_default=evento&c_classe=837284&__pj0=0&__pj1=36cd41e96fcd065c47b49d18e46e3110).

Student: **[To be assigned]**
_____

## Background

**Background**  
In batch learning, it is commonly assumed that samples are independent and identically distributed (i.i.d.). However, this assumption does not hold in dynamic environments where data streams exhibit concept drifts and evolving distributions. Additionally, while much of the Streaming Machine Learning (SML) literature assumes independence among examples, real-world data streams often contain important temporal dependencies that should be adequately modeled. Ignoring these dependencies can lead to suboptimal model design and misleading evaluations.  

To address these challenges, we have developed Tenet, a novel benchmarking framework designed to evaluate data stream classifiers in non-i.i.d. scenarios. Tenet consists of a data stream generator and a baseline model, where the generator introduces temporal dependencies into commonly used data streams for SML evaluation. The framework has demonstrated effectiveness in modeling dependencies and causal structures across various streaming scenarios. However, its current implementation primarily focuses on deterministic temporal dependencies. Indeed, the current version of the temporal injection follows the formula:

$y_t^{*} = mode (y_t, y_{t-1}, y_{t-2})$

Further details on the existing framework and its implementation can be found in the corresponding paper available in the repository. 

## Goals and Objectives

This project aims to extend Tenet to support multi-order dependencies and introduce stochastic modeling techniques to better capture real-world uncertainties in data streams. Specifically, the objective is to explore alternative functions beyond the mode (potentially considering more past labels) and introduce randomness in switching between functions. For instance, a concept drift could change the function governing temporal dependency injection.

The specific objectives of the project are:

* Implement deterministic temporal injection in CapyMOA library (wrapper from River versions are also acceptable).
* Extend the approach by incorporating a stochastic Temporal Injection methodology and evaluating temporal dependencies of orders greater than two.
* Compare the introduced temporal dependencies against the deterministic approach using Auto-Correlation Function (ACF), Partial Auto-Correlation Function (PACF), and decision boundary analysis concerning past labels.
* Conduct experiments with Hoeffding Tree and Adaptive Random Forest in CapyMOA, evaluating their performance on streams with both deterministic and stochastic temporal dependencies on different temporal order of the Temporal Injection.

## Datasets

The dataset used will include synthetic common SML data streams, specifically SEA, STAGGER, Sine1, and Sine2.

## Evaluation metrics

The metrics used for comparison will be:

* Run-time: measurement of the time required to complete training and prediction.
* Performance metrics: to assess the quality of the model.
* Memory Utilization: amount of RAM required during execution.

Moreover, visual plots will be used for the analysis of the impact of the Temporal Injection, similar to the approach used in the Tenet paper.

## Deliverable 

A comprehensive report detailing the methodology, extensions implemented for the Temporal Injection, and the experimental results with a comparative analysis of the enhanced framework’s performance against baseline models. 

The project will also include the implemented code and dataset specifications for reproducibility.

_____
## Note for Students

* Clone the created repository offline;
* Add your name and surname into the Readme file;
* Make any changes to your repository, according to the specific assignment;
* Add a `requirement.txt` file for code reproducibility and instructions on how to replicate the results;
* Commit your changes to your local repository;
* Push your changes to your online repository.
