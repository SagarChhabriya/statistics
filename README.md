# Statistics

## Introduction to Statistics
1. [Chapter 1](#chapter-1)
   Summary Statistics
    - What is stats?
    - Descriptive vs inferential stats
    - Measures of center
    - Measures of spread
2. [Chapter-2](#chapter-2)
  Probability and Distributions
    - What are the chances
    - Conditional Probability
    - Discrete Distributions
    - Continuous Distributions


## Chapter-1
- What is statistics: The practice and study of collecting and analyzing data.
- Two main branches of statistics
  - Descriptice/summary statistics: describing or summarizing our data
  - Inferential statistics: collect a sample of data, and apply the results to the population that the sample represents.
  - ![image](https://github.com/user-attachments/assets/bf5ec809-292a-469e-ad40-d19dd05c380a)
 
- What statistics can do?
    - Allows us to answer practical questions:
      - What is the average salary in the USA?
      - How many customer inquires is a company likely to receive per week?

    - It has applications across society:
        - Developing safer products such as cars or airplanes
        - Help governements understand the needs of a population

- Limitations of Statistics
    - Statistics requires specific, measurable questions:
        - Is rock mucs more popular than jazz?
        - On average, do women live longer than man?
    - We can's use stats to find out **why** relationships exist.

#### Types of data
- Numerical: Continuous | Interval/count
- Categorical: Nominal  | Oridnal


#### Descriptive vs Inferential 
- Descriptive stats describes or summarize data
- Inferential stats usa a sample to draw conclusions about population (How many people purchase clothing following social media?)



## Measuers of Center

|Name | Description|
|-----|----------------------------------------|
|Mean | sum of all values / count of all values|
|Median|Middle value |
|Mode| Most frequest value|
|Visualization| Histograms, KDE (kernel density estimation) plots|


## Measures of spread
|Name| Description|
|----|------------|
|Range|maximum - minimum|
|Variance|value - mean|
|Standard Deviation|√variance|
|Quartiles|Splitting the data into four equal parts|
|Interquartile Range (IQR)| 3rd Quratile - 1st Quartile|
|Visualizations|Boxplot|

Standard deviation close to zero = data clustered around the mean

![image](https://github.com/user-attachments/assets/7637335a-3bd9-407b-afa9-88f4bf4f5ef1)



## Chapter-2

#### What are the chances
![image](https://github.com/user-attachments/assets/c74b96e9-b61c-4340-a93b-f3a19e1e2031)<br><br>
![image](https://github.com/user-attachments/assets/d0a53b3c-097b-4d0e-ab63-ad99a10a5ef0)<br><br>

#### Independent Probability
Two events are **independent** if the probability of the second event **does not** change based on the outcome of the first event.

![image](https://github.com/user-attachments/assets/7ba1471e-6224-4b4e-95b5-15898d93e477) <br><br>
![image](https://github.com/user-attachments/assets/aa7794c0-f42c-4a8a-9149-24f70655da40) <br><br>


#### Conditional Probability
Conditional probability is used to calculate the probability of dependent events. The probability of one event is **conditional** on the outcome of another.
![image](https://github.com/user-attachments/assets/3007c70e-3ee9-487b-a23d-5fcb2da1f940) <br><br>

#### Dependent Events:
![image](https://github.com/user-attachments/assets/1f6bfe3a-95ab-4384-861b-a2e5763e2e25)<br>


**The probabitlity that claire is picked second depends on who gets picked first. If claire is picked first, there is 0% that claire will be picked second. If someone else is picked first, there's a 33% probability that the  Claire will be picked second.**

#### Conditional Probability Using Venn Diagrams
![image](https://github.com/user-attachments/assets/4c723d6d-cfc1-4f60-9b36-fe501f766d5b)

```Replace 161 of diagram with 181```
What are the number of orders for kitchen products where each order is greater than $150?

![image](https://github.com/user-attachments/assets/6f415d16-0012-44c9-aa62-3184ed2232d8)

#### The formula for conditional probability is given by:

The formula for conditional probability is:

    P(A | B) = P(A ∩ B) / P(B)

where:

- `P(A | B)` is the probability of event `A` given that event `B` has occurred.
- `P(A ∩ B)` is the probability that both events `A` and `B` occur.
- `P(B)` is the probability of event `B`.
#### Dependent VS Independent
![image](https://github.com/user-attachments/assets/49d4c125-31a3-4269-ac0e-b5da07c6e2e9)


#### Probability Distributions
`Distribution` The possible values a variable can take and how frequently they occur.

Probability distributions are statistical functions that describe the likelihood of obtaining possible values that a random variable can take. 
1. Discrete Probability Distribution
It models the probabilities of random variables that can have discrete values as outcomes. A discrete random variable is a random variable that has countable values, such as a list of non-negative integers. Discrete probability functions are also known as probability mass functions.<br><br>

Example: If you’re counting the number of books that a library checks out per hour, you can count 15 or 16 books, but nothing in between.

Discrete Probability Distributions can further be divided into

   1. Binomial Distribution
   2. Multinomial Distribution
   3. Bernoulli Distribution
   4. Negative Binomial Distribution
   5. Poisson Distribution
   6. Geometric Distribution
   7. Hypergeometric Distribution

2. Continuous Probability Distribution
It models the probabilities of the possible values of a continuous random variable. A continuous random variable is a random variable with a set of possible values that are infinite and uncountable. Continuous variables are often measurements on a scale, such as weight and temperature. Continuous probability functions are also known as probability density functions.
<br><br>

#### Discrete Distributions
Statistical inference requires assumptions about the probability distribution (i.e., random mechanism, sampling model) that generated the data. For example, for a t-test, we assume that the sample mean follows a normal distribution. Some common distributions used for discrete data are introduced in this section.<br><br>

Recall, a random variable is the outcome of an experiment (i.e., a random process) expressed as a number. We tend to use capital letters near the end of the alphabet (X, Y, Z, etc.) to denote random variables. Random variables are of two types: discrete and continuous.

![image](https://github.com/user-attachments/assets/af1d9bc2-0f9d-48e8-a0a4-093007d6886a)



