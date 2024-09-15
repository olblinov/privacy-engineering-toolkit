# Differential Privacy

## General

## Global

## Local
- [How your data is secured(by a coin toss)](https://towardsdatascience.com/how-your-data-is-secured-by-a-coin-toss-c933f9e13d4a)
- [Local vs Global Differential Privacy](https://blog.openmined.org/basics-local-differential-privacy-vs-global-differential-privacy/)
- [Google RAPPOR](https://github.com/google/rappor/tree/master?tab=readme-ov-file)
  - [RAPPOR & Diffrential Privacy](https://florian.github.io/differential-privacy/)
  - [Building a RAPPOR with the Unknown: Privacy-Preserving Learning of Associations and Data Dictionaries](https://arxiv.org/pdf/1503.01214v1.pdf)
- [Differential privacy in (a bit) more detail](https://desfontain.es/privacy/differential-privacy-in-more-detail.html)

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