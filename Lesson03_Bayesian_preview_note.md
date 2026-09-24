# Lesson 3
## Bayesian Analysis and Risk Assessment in Genetic Counseling and Testing
### Case 1
> We have a patient with two brothers who have Kennedy Disease,
> which is an X-linked spinal and bulbar muscular atrophy. The disease is caused by
> a CAG trinucleotide expansion in the androgen receptor (AR) gene. Since
> both brothers are affected, we know patient's mother is an obligated carrier of
> the disease allele. The patient herself has three healthy sons.
>  Now we have to calculate the probability of the patient being a carrier.

For this question, we have to start with drawing a pedigree:

<img width="350" height="219" alt="image" src="https://github.com/user-attachments/assets/51c08e81-7302-4c93-88c8-8e99f492e679" />

Since we are not sure if patient herself is a carrier or not, we have two hypothesis:
1. She is a carrier
2. She is not a carrier

Now we use a table to first calculate the prior probability for each hypothesis,
 which is now in this case she is a carrier/non-carrier. Theoretically, 
 the probability of her being a carrier/non-carrier should be both 1/2 PRIOR to any other
 conditions. Because she can inherit either of her mother's X chromosome alleles.

|Hypothesis|Carrier|Non-carrier|
|----------|-------|-----------|
|Prior Probability|1/2|1/2|

And now, let's calculate the conditional probability of her three sons are all healthy:
1. If she is a carrier, her three sons ALL being healthy are independent incidents.
   For each son, she has 1/2 probability to pass the mutant gene to him.
   So the probability should be ${1/2 \times 1/2 \times 1/2}$, which is 1/8.
2. If she is a non-carrier, her three sons ALL being healthy are 100% percent.
   In this case, the conditional probability would be 1

|Hypothesis|Carrier|Non-carrier|
|----------|-------|-----------|
|Conditional Probability|1|1|

Now let's put the probabilities together.
* The probability of her being a carrier AND having three healthy son is ${1/2 \times 1/8 = 1/16}$
* The probability of her being a non-carrier AND having three healthy son is ${1/2 \times 1 = 1/2}$

|Hypothesis|Carrier|Non-carrier|
|----------|-------|-----------|
|Joint Probability|1/16|1/2|

And now we want to calculate the probability of her being a carrier/non-carrier AFTER
we consider the conditions, which is the posterior probability. 
First thing first, let's simplify her being a carrier as event A; her having three healthy
sons as event B.
Considering her being a carrier AND having three healthy sons 
would be: $\[P(\text{A}) \times P(\text{B})\]$. Now we want to see its probability 
ratio versus both hypothesis combined, in this case: 

$$\frac{P(A)P(B)}{P(A)P(B) + P(A)}$$

Therefore:
* Numerator: $\[P(\text{Carrier}) \times P(3 \text{ healthy kids if Carrier})\]$

* Denominator: $\{[P(\text{Carrier}) \times P(3 \text{ healthy kids if Carrier})]+[P(\text{Not Carrier}) \times P(3 \text{ healthy kids if Not Carrier})]\}$

(Notice that WHEN P(A) IS EXACTLY 1/2:

$$\frac{P(A)P(B)}{P(A)P(B) + P(A)} = \frac{P(B)}{1 + P(B)} = \frac{1/8}{1+1/8}$$

Also notice that probability of patient being a non-carrier is 

$$[P(A) \times P(B)] + [(1 - P(A)) \times 1]$$
)

These are just for simplifying during which case P(A) is 0.5, so DON'T ASSUME IT IS A STANDARD ALTERNATIVE!!!

Plug in values and see the results.

The results should be like:

|Hypothesis|Carrier|Non-carrier|
|----------|-------|-----------|
|Prior Probability|1/2|1/2|
|Conditional Probability|1|1|
|Joint Probability|1/16|1/2|
|Posterior Probability|(1/16)/(1/16 + 1/2)=1/9|(1/2)/(1/16 + 1/2)=8/9|

* Things to bring to TA session: For case 1, would it be possible for only one of her brothers to have Kennedy disease?

### Case 2
> Consider the pedigree shown in Figure 2A, in which the consultand is pregnant with her first child and has a family history of cystic fibrosis (CF). CF is caused by mutations in the cystic fibrosis transmembrane conductance regulator (CFTR) gene [OMIM Nos. 602421;219700 (CF)]. The consultand is an unaffected European
Caucasian and her brother died years earlier of complications of CF. She undergoes carrier testing for the 25
mutations recommended by the American College of
Medical Genetics (ACMG) CF screening guidelines,6,7
which detects 90% of disease alleles in European Cauasians. She tests negative for all 25 mutations. What is
her carrier risk?

<img width="297" height="249" alt="image" src="https://github.com/user-attachments/assets/cabbe393-a628-41c0-9a3a-c55b0381a77c" />

Here, the conditional probability would be she has a negative test result. Therefore, the chart should be:

|Hypothesis|Carrier|Non-carrier|
|----------|-------|-----------|
|Prior Probability|2/3|1/3|
|Conditional Probability|1/10|1|
|Joint Probability|1/15|1/3|
|Posterior Probability|(1/15)/(1/15 + 1/3)=1/6|(1/3)/(1/15 + 1/3)=5/6|

> Now, suppose in the second example that
the consultand’s husband is Ashkenazi Jewish, that he
has no family history of CF, and that he tests negative for
all 25 mutations in the panel. What is his carrier risk?
The carrier risk in Ashkenazi Jewish populations, and
therefore the husband’s prior carrier risk in the absence
of a family history, is approximately 1/25. Thus his prior
probability of being a non-carrier is 24/25. The ACMG
screening guidelines panel of 25 mutations detects 97%
of CF mutations in Ashkenazi Jewish populations, so the
conditional probability of a negative test, under the hypothesis that he is a carrier, is 3/100.

The chart should be like:

|Hypothesis|Carrier|Non-carrier|
|----------|-------|-----------|
|Prior Probability|1/25|24/25|
|Conditional Probability|3/100|1|
|Joint Probability|3/2500|24/25|
|Posterior Probability|(3/2500)/(3/2500 + 24/25)=1/801|(24/25)/(3/2500 + 24/25)=800/801|

### Case 3
>  Consider the
pedigree shown in Figure 4A, in which the maternal uncle
(I-2) and brother (II-1) of the consultand (II-2) were affected with Duchenne muscular dystrophy (DMD), a severe X-linked recessive disease caused by mutations in
the DMD gene (OMIM Nos. 300377; 310200). With an
affected brother and son, the consultand’s mother (I-1) is
essentially an obligate carrier. In addition, I-1 has an
elevated level of creatine phosphokinase (CPK) in her
serum, which occurs in 67% of DMD carrier women.
Hence, the sensitivity of the serum CPK test for carrier
status in women is 67%. Since 5% of non-carrier women
have an abnormal serum CPK, the specificity of the
serum CPK test for carrier status in women is 95%.

<img width="395" height="281" alt="image" src="https://github.com/user-attachments/assets/15c00586-e2d7-48b2-9ae2-8cdaf6366f24" />

In this case, the chart would be like:

|Hypothesis|Carrier|Non-carrier|
|----------|-------|-----------|
|Prior Probability|1/2|1/2|
|Conditional Probability(negative)|0.33|0.95|
|Joint Probability|0.165|0.475|
|Posterior Probability|(0.165)/(0.64)=0.26|(0.475)/(0.64)=0.74|

### Generalized Bayesian Analysis
The prior probability of a particular hypothesis is designated as $\alpha$,
and the prior probability of an alternative
hypothesis is designated as (1 - $\alpha$). The probability that
specific subsequent information would occur if we assume that the particular hypothesis is true (ie, the conditional probability for the particular hypothesis), is designated as $\beta$. 
The probability that specific subsequent
information would occur if we assume that the alternative
hypothesis is true (ie, the conditional probability for the
alternative hypothesis), is designated as $\gamma$.

<img width="678" height="663" alt="image" src="https://github.com/user-attachments/assets/960e1b6d-04b1-4c5e-8cf8-d303220a2b7e" />

<img width="492" height="625" alt="image" src="https://github.com/user-attachments/assets/e5f97dd4-ad12-4cf2-b9d5-5620784681e5" />

Because posterior probabilities rest in part on
prior probabilities, genetic risk assessments must integrate all relevant and available information, including
ethnicity, family history, clinical presentations, genetic
testing results for other family members, and previous
genetic testing results for the consultand. The sensitivity
of a genetic test for a particular individual, which determines the conditional probability of a negative result under the hypothesis of carrier or disease status, is frequently altered by additional information. For example, if
a non-Hispanic Caucasian consultand, whose sibling is
affected with cystic fibrosis, is tested only for the $\Delta$ F508
mutation in CFTR the sensitivity of the test is approximately 70%. Hence the conditional probability of a
negative result under the hypothesis of carrier status is
approximately 30%. However, suppose that the affected
sibling is found to be homozygous for the $\Delta$ F508 mutation. Assuming the parents are unaffected, the sensitivity
of the test for the consultand increases to essentially
100%. This is because the prior probability of carrying a
CFTR mutation comprises the $\Delta$ F508 mutation only.
