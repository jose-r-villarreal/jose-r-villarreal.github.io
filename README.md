# Odds Ratio as an estimator of Relative Risk

### *by* Jose Romeo Villarreal
### June 22, 2020

## Introduction
Relative Risk (RR) is a parameter frequently reported in cohort studies. It indicates the risk of a certain outcome with a specific risk factor in relation to a control group without such risk factor. The case-control study design does not allow the the calculation of the RR, so instead the Odds Ratio (OR) is used. When the prevalence of the outcome is low, the OR is a good approximation to the RR.

> For rare outcomes, the OR approximates the RR.

## Relative Risk
As stated above, the RR indicates the risk of an outcome when a specific risk factor is present, compared with the risk for such outcome in the absence of the risk factor. Suppose we are interested in finding if obesity is associated with increased risk for being infected with COVID-19. To find out, we will conduct a prospective study. According to official data, there were 5 thousand confirmed new cases of COVID-19 in Mexico on June 18th, 2020. We are going to suppose that 5,000 is going to be the average number of new cases during the next 30 days. That means we should expect about 150,000 new cases. For a country with a population of 130 million, that represents a monthly incidence of 115 new cases for every 100 thousand persons. That would be the average risk of being diagnosed with COVID-19 in Mexico. To know if obese subjects are at increased risk of being COVID-19, we will recruit 100 thousand obese subjects (BMI > 30 kg/m^2^) and 100 thousand subjects with normal weight (BMI < 25 kg/m^2^); all of them without COVID-19. Then we will see how many of each group are diagnosed with COVID-19 during the next 30 days. The results can be then be presented as a contingency table in the following way:

* A: number of obese subjects who were diagnosed with COVID-19 during the study
* B: number of obese subjects who were **not** diagnosed with COVID-19 during the study
* C: number of normal weight subjects who were diagnosed with COVID-19 during the study
* D: number of normal weight subjects who were **not** diagnosed with COVID-19 during the study

Outcome | Obese | Normal Weight | Total
---|---|---|---
COVID-19 | A | C | A + C
Not infected | B | D | B + D
Total | A + B | C + D | A + B + C + D

Suppose the outcome is the following:

Outcome | Obese | Normal Weight | Total
---|---|---|---
COVID-19 | 200 | 70 | 270
Not infected | 99,800 | 99,930 | 199,730
Total | 100,000 | 100,000 | 200,000

The risk for being infected with COVID-19 for an obese subject would be $$\displaystyle \frac{A} {A + B} = \displaystyle \frac{200} {200 + 99,800}$$
which would equal 0.2 % (or 200 cases for every 100 thousand persons).

The risk for a normal weight subject would be $$\displaystyle \frac{C} {C + D} = \displaystyle \frac{70} {70 + 99,930}$$
which would equal 0.07 % (or 70 cases for every 100 thousand persons).

The RR for being infected with COVID-19 for obesity can be calculated according to the following formula:

$$\displaystyle \frac{A} {A + B} \div \displaystyle \frac{C} {C + D}$$

which is simply the risk of being infected with COVID-19 for a person with obesity divided by the risk for a person with normal weight. Substituting the letters with numbers:

$$\displaystyle \frac{200} {200 + 99,800} \div \displaystyle \frac{70} {70 + 99,930} = 2.86$$

This means the risk of a person with obesity to be infected with COVID-19 is about 2.86 times the risk of a person with normal weight (according to these make-up data).

## Odds Ratio

If you think it would be unconvenient to recruit 100 thousand people with obesity, another 100 thousand with normal weight, and then follow them up for 30 days to see how many of them are diagnosed with COVID-19, you are right! The case-control design addresses this inconvenience. Instead of recruiting thousands of obese and normal weight subjects, we can recruit a 200 people with recent diagnosis of COVID-19, other 200 people without COVID-19, and see how many of them have obesity and how many of them have normal weight. Let's suppose that those 200 COVID-19 cases and 200 non-infected controls are representative of the COVID-19 and the non-infected subjects, respectively, of the previous hypothetical study. We would get the following contingency table:

Outcome | Obese | Normal Weight | Total
---|---|---|---
COVID-19 | 148 | 52 | 200
Not infected | 100 | 100 | 200
Total | 248 | 152 | 400

Because of the study design, in a case control study we cannot really know the risk of the outcome. We can only know the odds of having the presumed risk factor given you had or did not had the outcome. The OR can be calculated by the following formula:

$$\displaystyle \frac{A} {B} \div \displaystyle \frac{C} {D} = \displaystyle \frac{148} {100} \div \displaystyle \frac{52} {100} = 2.85$$

The OR is almost the same as the RR.

## Effect of High Prevalence on RR and OR

Let's suppose an extreme scenario. The relative risk for being infected with obesity will remain constant, but we will suppose half the population is going to become infected with COVID-19 the next month. This catastrophic scenario simplifies the task to conduct a prospective cohort study. Now we do not need to recruit 100 thousand subjects per cohort to expect a couple of hundreds of COVID-19 new cases. We can now limit ourselves to recruit 200 subjects with obesity, and another 200 subjects with normal weight.

Outcome | Obese | Normal Weight | Total
---|---|---|---
COVID-19 | 148 | 52 | 200
Not infected | 52 | 148 | 200
Total | 200 | 200 | 400

$$\displaystyle \frac{148} {148 + 52} \div \displaystyle \frac{52} {52 + 148} = 2.85$$

The RR is still about 2.85 (we specifically designed the simulated data maintain a constant RR). 

Now let's suppose that we didn't perform such prospective study, the catastrophic month with 50 % incidence did happen a now we got rid of the coronavirus for good. And now we want to know afterwards if obesity was a risk factor for being infected with COVID-19 during that terrible month. So now we perform a case control study with 200 known COVID-19 cases and 200 not-infected controls. If the sample recruited is representative of the same population of the previous hypothetical prospective study, we should expect a similar contingency table. In fact, let's pretend the contingency table turns out to be exactly equal. Now we will calculate the OR:

$$\displaystyle \frac{148} {52} \div \displaystyle \frac{52} {148} = 8.1$$

With the same numbers, now we got a much different OR! What did change? Let's take a closer look at the formulas of RR and OR.

RR formula:

$$\displaystyle \frac{A} {A + B} \div \displaystyle \frac{C} {C + D}$$

OR formula:

$$\displaystyle \frac{A} {B} \div \displaystyle \frac{C} {D}$$

The numerators in both formulas are the same (A and C), which are the number of cases with or without the presumed risk factor. But the denominators are different. For the RR, the denominators are A + B and C + D, which correspond to the total of exposed and not exposed to the risk factor. For the OR, the denominators are simply B and D, the number of persons without the outcome of interest with and without the presumed risk factor. In the specific case were the outcome of interest has a low frequency, A + B is almost the same as B (because A is low relative to B). Likewise, C + D would be almost the same as D (again, because C is low relative to D). Therefore, the lower the frequency of the outcome, the more similar the OR would be to the RR. However, as the frequency of the outcome increases, the OR will overestimate the RR.

## Conclussion
Does this mean that the OR is useless when the outcome has a high frequency? Not at all! The OR is a parameter with its own interpretation. What this means is that for low frequency outcomes, both parameters will have a tendency to be near equal. Therefore, in those cases we can assume the OR is the same as the RR. When this condition is not satisfied, we should be careful in the interpretation of the OR and keep in mind it will not be the same as the RR.

> I love Ivette Lopez, MD, the most beautiful woman and hardworking student on Earth!

