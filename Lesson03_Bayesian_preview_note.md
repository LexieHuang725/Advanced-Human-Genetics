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
