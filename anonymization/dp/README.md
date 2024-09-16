# Differential Privacy

## General

- [Local vs Global Differential Privacy](https://blog.openmined.org/basics-local-differential-privacy-vs-global-differential-privacy/)

## Global

## Local
### Theory 
- [Differential privacy in (a bit) more detail](https://desfontain.es/privacy/differential-privacy-in-more-detail.html)

### Implementation


- [How your data is secured(by a coin toss)](https://towardsdatascience.com/how-your-data-is-secured-by-a-coin-toss-c933f9e13d4a)
<details>
  <summary>Coin toss local DP</summary>
  Suppose you want to do a survey to know how many people are illegal drug users. If you naively go out and ask people whether they're using illegal drugs, many will lie to you. So you devise the following mechanism. The participants no longer directly answer the question "have you consumed illegal drugs in the past week?". Instead, each of them will flip a coin, without showing it to you.

  - On heads, the participant tells the truth (Yes or No).
  - On tails, they flip a second coin. If the second coin lands on heads, they answer Yes. Otherwise, they answer No.

  How is this better for survey respondents? They can now answer Yes without revealing that they're doing something illegal. When someone answers Yes, you can't know their true answer for sure. They could be actually doing drugs, but they might also have answered at random.

  Let's compute the probabilities of each answer for a drug user.
  - With probability 50%, they will say the truth and answer Yes.
  - With probability 50%, they will answer at random.
    - They then have another 50% chance to answer Yes, so 25% chance in total.
    - Similarly, in total, they have a 25% chance to answer No.

  All in all, we get a 75% chance to answer Yes and a 25% chance to answer No. For someone who is not doing drugs, the probabilities are reversed: 25% chance to answer Yes and 75% to answer No. Using the notations from earlier:

  - ℙ[A(Yes)=Yes]=0.75, ℙ[A(Yes)=No]=0.25
  - ℙ[A(No)=Yes]=0.25, ℙ[A(No)=No]=0.75

  Now, 0.75 is three times bigger than 0.25. So if we choose ε such as e^ε=3 (that's ε≃1.1), this process is ε-differentially private. So this plausible deniability translates nicely in the language of differential privacy.

  Of course, with a differentially private process like this one, you're getting some noise into your data. But if you have enough answers, with high probability, the noise will cancel itself out. 

  > Suppose you have 1000 answers in total: 400 of them are Yes and 600 are No. About 50% of all 1000 answers are random, so you can remove 250 answers from each count. In total, you get 150 Yes answers out of 500 non-random answers, so about 30% of Yes overall.

  What if you want more privacy? Instead of having the participants say the truth with probability 50%, you can have them tell the truth 25% of the time. What if you want less noise instead, at the cost of less protection? Have them tell the truth 75% of the time. Finding out ε and quantifying the noise for each option is left as an exercise for the reader =)
</details>


#### Google RAPPOR
  - Google
    - [GitHub repo (https://github.com/google/rappor)](https://github.com/google/rappor)
    - [RAPPOR Data Flow (https://google.github.io/rappor/doc/data-flow.html)](https://google.github.io/rappor/doc/data-flow.html)
    - Erlingsson, Úlfar, Vasyl Pihur, and Aleksandra Korolova. [Rappor: Randomized aggregatable privacy-preserving ordinal response.](https://arxiv.org/pdf/1407.6981) Proceedings of the 2014 ACM SIGSAC conference on computer and communications security. 2014.
    - Fanti, Giulia, Vasyl Pihur, and Úlfar Erlingsson. [Building a RAPPOR with the unknown: Privacy-preserving learning of associations and data dictionaries.](https://arxiv.org/pdf/1503.01214) arXiv preprint arXiv:1503.01214 (2015).
  - Other sources:
    - [RAPPOR & Diffrential Privacy (https://florian.github.io/differential-privacy/)](https://florian.github.io/differential-privacy/)
    - [RAPPOR implementations (GitHub topics)](https://github.com/topics/rappor)

#### GitHub Repos

- [hharcolezi / multi-freq-ldpy](https://github.com/hharcolezi/multi-freq-ldpy)
  - Arcolezi, Héber H., et al. [Multi-Freq-LDPy: multiple frequency estimation under local differential privacy in python.](https://arxiv.org/pdf/2205.02648) European Symposium on Research in Computer Security. Cham: Springer Nature Switzerland, 2022.
- [Samuel-Maddock / pure-LDP](https://github.com/Samuel-Maddock/pure-LDP)
  - Cormode, Graham, Samuel Maddock, and Carsten Maple. [Frequency estimation under local differential privacy [experiments, analysis and benchmarks].](https://vldb.org/pvldb/vol14/p2046-cormode.pdf) arXiv preprint arXiv:2103.16640 (2021).
- [hharcolezi / ldp-protocols-mobility-cdrs](https://github.com/hharcolezi/ldp-protocols-mobility-cdrs)
  - Arcolezi H.H., Couchot JF., Bouna B.A., Xiao X. (2021) [Longitudinal Collection and Analysis of Mobile Phone Data with Local Differential Privacy](https://doi.org/10.1007/978-3-030-72465-8_3). In: Friedewald M., Schiffner S., Krenn S. (eds) Privacy and Identity Management. Privacy and Identity 2020. IFIP Advances in Information and Communication Technology, vol 619. Springer, Cham.
  - Arcolezi H.H., Couchot JF., Bouna B.A., Xiao X. (2021) [Random Sampling Plus Fake Data: Multidimensional Frequency Estimates With Local Differential Privacy](https://doi.org/10.1145/3459637.3482467). In Proceedings of the 30th ACM International Conference on Information and Knowledge Management (CIKM '21). November 1-5, 2021, Virtual Event, QLD, Australia. 
  - Arcolezi H.H., Couchot JF., Renaud D., Bouna B.A., Xiao X. (2022) [Differentially Private Multivariate Time Series Forecasting of Aggregated Human Mobility With Deep Learning: Input or Gradient Perturbation?](https://doi.org/10.1007/s00521-022-07393-0). Neural Computing and Applications, vol. 34, 13355–13369. 
  - Arcolezi H.H., Couchot JF., Bouna B.A., Xiao X. (2022) [Improving the Utility of Locally Differentially Private Protocols for Longitudinal and Multidimensional Frequency Estimates](https://doi.org/10.1016/j.dcan.2022.07.003). Digital Communications and Networks. 
  - Arcolezi, H. H., Cerna, S., Guyeux, C., & Couchot, J. F. (2021). [Preserving geo-indistinguishability of the emergency scene to predict ambulance response time](https://doi.org/10.3390/mca26030056) . Mathematical and Computational Applications, 26(3), 56.