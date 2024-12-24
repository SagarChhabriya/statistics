
### Case Studies

#### Case Study 1: **Exam Scores and Normal Distribution**
A teacher collects exam scores from a class of 40 students. The scores range from 40 to 100. The teacher then takes random samples of 30 students and calculates the mean exam score for each sample. After taking 50 such samples, the teacher observes that the sample means are distributed in a roughly bell-shaped curve. The teacher is interested in determining whether the average exam score of the entire class follows a normal distribution.

1. **Mathematical Question**:  
   What is the expected shape of the distribution of sample means based on the Central Limit Theorem (CLT)?
   
2. **Programmatic Question**:  
   Write a Python function to simulate the process of taking 50 random samples of 30 students each and calculate the mean of each sample. Plot the distribution of the sample means.

---

#### Case Study 2: **Voting Preferences in a City**
A political analyst wants to estimate the proportion of voters in a city who prefer a certain candidate. The analyst randomly selects 100 voters from the city and asks them who they will vote for. The analyst repeats this process 50 times, collecting 50 samples of 100 voters.

1. **Mathematical Question**:  
   What is the sampling distribution of the sample proportions? Assuming the true proportion of voters preferring the candidate is 0.3, calculate the expected mean and standard deviation of the sampling distribution.
   
2. **Programmatic Question**:  
   Write a Python function to simulate taking 50 samples of 100 voters each, where each voter has a 30% chance of preferring the candidate. Calculate the sample proportions and plot the distribution of these proportions.

---

#### Case Study 3: **Hospital Readmission Rates**
A healthcare provider is investigating the rate at which patients are readmitted to the hospital within 30 days after discharge. The provider randomly selects 200 patients and finds that 30% of them are readmitted within 30 days. The provider repeats this process 100 times, taking 100 samples of 200 patients each.

1. **Mathematical Question**:  
   Calculate the probability of observing exactly 60 readmissions out of 200 patients using the binomial distribution. Assume the probability of readmission is 0.3.
   
2. **Programmatic Question**:  
   Write a Python program that simulates 100 samples of 200 patients, where each patient has a 30% chance of being readmitted. Calculate the proportion of patients readmitted for each sample, and then plot the distribution of these proportions.

---

#### Case Study 4: **Customer Satisfaction Survey**
A company conducts a customer satisfaction survey for its product. Out of 500 surveyed customers, 75% report being satisfied. The company then wants to estimate the true satisfaction rate of all customers by repeatedly taking random samples of 50 customers.

1. **Mathematical Question**:  
   How does the binomial distribution apply to this situation? Calculate the expected value and variance of the number of satisfied customers in a sample of 50.
   
2. **Programmatic Question**:  
   Write a Python function to simulate 1000 samples of 50 customers, where each customer has a 75% chance of being satisfied. Calculate the number of satisfied customers in each sample and plot the distribution.

---

#### Case Study 5: **Average Income in a Region**
A researcher is interested in estimating the average income of households in a specific region. The researcher randomly selects 100 households and records their income. The researcher repeats this process 40 times, each time selecting a sample of 100 households.

1. **Mathematical Question**:  
   What is the sampling distribution of the sample means? If the population mean is \$50,000 and the standard deviation is \$10,000, calculate the expected mean and standard error of the sample means.
   
2. **Programmatic Question**:  
   Write a Python function that simulates 40 samples of 100 households. Assume the population mean is \$50,000 and the population standard deviation is \$10,000. Calculate the sample means for each sample and plot the distribution of the sample means.

---

### Solutions

#### Solution 1: **Exam Scores and Normal Distribution**
1. **Expected Shape of the Distribution of Sample Means**:  
   According to the Central Limit Theorem (CLT), regardless of the original population distribution, the distribution of the sample means will approach a normal distribution as the number of samples increases, provided the sample size is large enough (n ≥ 30). Thus, for 50 samples of 30 students each, the distribution of the sample means will be approximately normal.

2. **Python Code to Simulate the Sampling Process**:

```python
import numpy as np
import matplotlib.pyplot as plt

# Simulate 50 samples of 30 students' exam scores
np.random.seed(0)
sample_means = []
for _ in range(50):
    sample = np.random.uniform(40, 100, 30)  # Exam scores between 40 and 100
    sample_means.append(np.mean(sample))

# Plot the distribution of sample means
plt.hist(sample_means, bins=10, edgecolor='black')
plt.title('Distribution of Sample Means')
plt.xlabel('Sample Mean Exam Score')
plt.ylabel('Frequency')
plt.show()
```

---

#### Solution 2: **Voting Preferences in a City**
1. **Sampling Distribution of the Sample Proportions**:  
   The sampling distribution of sample proportions is approximately normal, with the mean equal to the true population proportion (0.3) and the standard deviation given by:
   
$$
\sigma_{\hat{p}} = \sqrt{\frac{p(1-p)}{n}}
$$

   where $p = 0.3$ and $n = 100$.

3. **Python Code to Simulate the Sampling Process**:

```python
import numpy as np
import matplotlib.pyplot as plt

# Simulate 50 samples of 100 voters, with 30% probability of voting for the candidate
np.random.seed(0)
sample_proportions = []
for _ in range(50):
    sample = np.random.binomial(1, 0.3, 100)  # 1 for success (vote for candidate), 0 for failure
    sample_proportions.append(np.mean(sample))

# Plot the distribution of sample proportions
plt.hist(sample_proportions, bins=10, edgecolor='black')
plt.title('Distribution of Sample Proportions')
plt.xlabel('Proportion of Voters')
plt.ylabel('Frequency')
plt.show()
```

---

#### Solution 3: **Hospital Readmission Rates**
1. **Probability of Observing 60 Readmissions Out of 200 Patients**:  
   We can use the binomial distribution to calculate the probability of exactly 60 readmissions, where $n = 200$ and $p = 0.3$:
 
$$
P(X = 60) = \binom{200}{60} \cdot 0.3^{60} \cdot 0.7^{140}
$$
   This can be calculated using the `scipy.stats.binom` module.

2. **Python Code to Simulate the Sampling Process**:

```python
import numpy as np
import matplotlib.pyplot as plt

# Simulate 100 samples of 200 patients, with 30% probability of readmission
np.random.seed(0)
readmission_proportions = []
for _ in range(100):
    sample = np.random.binomial(200, 0.3)  # Number of readmissions in 200 patients
    readmission_proportions.append(sample / 200)

# Plot the distribution of readmission proportions
plt.hist(readmission_proportions, bins=10, edgecolor='black')
plt.title('Distribution of Readmission Proportions')
plt.xlabel('Proportion of Readmitted Patients')
plt.ylabel('Frequency')
plt.show()
```

---

#### Solution 4: **Customer Satisfaction Survey**
1. **Application of the Binomial Distribution**:  
   Since each customer either reports being satisfied or not, the situation follows a binomial distribution. For a sample size of 50 and a probability of success (satisfaction) of 0.75, we can calculate the expected number of satisfied customers and the variance:

$$
\mu = n \cdot p = 50 \cdot 0.75 = 37.5
$$

$$
\sigma^2 = n \cdot p \cdot (1 - p) = 50 \cdot 0.75 \cdot 0.25 = 9.375
$$

2. **Python Code to Simulate the Sampling Process**:

```python
import numpy as np
import matplotlib.pyplot as plt

# Simulate 1000 samples of 50 customers, with 75% probability of satisfaction
np.random.seed(0)
satisfaction_counts = []
for _ in range(1000):
    sample = np.random.binomial(50, 0.75)  # Number of satisfied customers in 50
    satisfaction_counts.append(sample)

# Plot the distribution of satisfied customers
plt.hist(satisfaction_counts, bins=10, edgecolor='black')
plt.title('Distribution of Satisfied Customers')
plt.xlabel('Number of Satisfied Customers')
plt.ylabel('Frequency')
plt.show()
```

---

#### Solution 5: **Average Income in a Region**
1. **Sampling Distribution of Sample Means**:  
   According to the Central Limit Theorem, the sampling distribution of the sample means will be approximately normal. The expected mean of the sample means will be the population mean (\$50,000), and the standard error is given by:

$$
\text{SE} = \frac{\sigma}{\sqrt{n}} = \frac{10000}{\sqrt{100}} = 1000
$$

2. **Python Code to Simulate the Sampling Process**:

```python
import numpy as np
import matplotlib.pyplot as plt

# Simulate 40 samples of 100 households' income
np.random.seed(0)
sample_means = []
for _ in range(40):
    sample = np.random.normal(50000, 10000, 100)  # Normal distribution with mean 50000 and std 10000
    sample_means.append(np.mean(sample))

# Plot the distribution of sample means
plt.hist(sample_means, bins=10, edgecolor='black')
plt.title('Distribution of Sample Means (Income)')
plt.xlabel('Sample Mean Income')
plt.ylabel('Frequency')
plt.show()
```
