Group 3
# **A Data Analytics Project with Python: Analyzing Medical Data**
https://medium.com/@natashanewbold/a-data-analytics-project-with-python-17614afa956b

> [**Disclaimer:**]
> The instructions and code used in the project are based on the provided guidelines

## **Introduction**

The project "A Data Analytics Project with Python: Analyzing Medical Data" explores how to make use of data analysis methods and Python programming tools to gather important information from medical datasets, particularly a tiny dataset of diabetic patients. It aims to introduce users with the application of Python in the analysis of medical data. Using Python modules including NumPy and Pandas, it offers a collaborative approach for statistical analysis, graphical representation, and predictive modeling. This project demonstrates the use of data analytics in the healthcare industry, where the abundance of data at hand may be utilized to enhance decision-making, optimize healthcare procedures, and improve patient outcomes. 

In line with this project, we have 11 columns from the datasets, indicating age, sex, BMI (body mass index), BP (average blood pressure), S1 to S6, which indicate different blood measurements, and the Y variable, which is the qualitative measure of disease progression over one year. This project intends to show how useful insights may be extracted from medical datasets using Python programming tools and data analysis approaches. Showcase Python's ability to handle intricate medical data that can help enhance healthcare analytics and make well-informed decisions.


## **Objectives**

* To describe the statistical analysis, visualizations, and modeling methods applied.
* To interpret and discuss the insights gained from the analysis.
* To explain the significance of the results in the context of the medical domain.
* To discuss the practical implications of the analysis in healthcare or medical research.


## **Methodology**

**Dataset Construction:** Created the diabetes.tab.text dataset with patient data (age, sex, BMI, average blood pressure, S1-S6 blood measures, and disease progression indicator Y).

**Coding Process:** Utilized Python to import libraries (pandas, numpy, matplotlib.pyplot) and load the dataset (df = pd.read_csv("diabetes.tab.txt", sep='/t')). Viewed dataset details using df.head() and df.info().

### **Tasks:**

**Task 1: Mean, Variance, and Standard Deviation Calculation**
Utilized numpy functions (mean(), var(), std()) to calculate for BP, sex, age, S1-S6, and Y. Printed results using print(f"Mean = {mean} Variance = {var} Standard Deviation = {std}").

**Task 2: Boxplots Based on Gender**
Used matplotlib.pyplot (plt) to create boxplots for BMI, BP, and Y based on gender. Set figure size with plt.figure(figsize=(10,2)). Executed plt.boxplot(df[' '], vert=False, showmeans=True) for desired values. Added grid with plt.grid(color='gray', linestyle='dotted') and displayed with plt.show().

**Task 3: Histograms for Age, Sex, BMI, and Y**
Utilized df[' '].hist(bins=15) to create histograms for age, sex, BMI, or Y. Labeled with plt.suptitle('--- distribution of diabetic patient') and plt.xlabel('---'). Displayed with plt.show().

**Task 4: Correlation Testing**
  Created scatter plots using plt.scatter(df[' '], df['Y']) for age or BMI. Set title with plt.title('--- vs. Y') and labels with plt.xlabel('---') and plt.ylabel('Y'). Displayed scatter plot with plt.show().


## **Result and Discussion**

**Task 1: Analyzing the mean, and variance**
The analysis delves into the descriptive statistics of numerous aspects in a dataset, most likely connected to diabetes patients.

**1. Age (AGE):**
     - Mean Age: 48.52 years
     - Variability (Variance): 171.85
     - Dispersion (Standard Deviation): 13.11

     - The average age of the individuals in the dataset is around 48 years, with a relatively small spread indicated by the standard deviation. Understanding the age distribution is crucial in medical studies as certain conditions may be age-related.

**2. Sex (SEX):**
   Mean Sex: 1.47 (assuming this is a binary variable)
   Variability (Variance): 0.25
   Dispersion (Standard Deviation): 0.50
   
   The mean suggests a binary encoding for gender, with a relatively low variance. This might indicate that the dataset is predominantly composed of one gender. Understanding gender distribution is important in medical research as some conditions may have gender-specific patterns.

**3. Blood Pressure (BP):**
   Mean BP: 94.65
   Variability (Variance): 191.30
   Dispersion (Standard Deviation): 13.83

   The average blood pressure is 94.65, and there is a notable variability as indicated by the high variance. Monitoring blood pressure is critical in diabetes management as it is often associated with cardiovascular complications.

**4. S1 to S6 (Derived Variables):**
   These variables represent different physiological measurements. Mean, Variability, and Dispersion for each variable.

   Understanding the means and variations in these physiological measurements is crucial for assessing the overall health of individuals with diabetes. Each of these variables likely plays a role in the progression and management of diabetes.

**5. Target Variable (Y):**
   Mean Y: 152.13
   Variability (Variance): 5943.33
   Dispersion (Standard Deviation): 77.09

   The target variable, denoted as “Y”, has a mean value of 152.13, indicating the average response variable in the dataset. The high variance suggests a wide range of values, which might be indicative of the heterogeneity in patient outcomes.

**Task 2: Boxplot Analysis**
A box plot graphically represents the dispersion of data values in the form of quartiles. It is capable of showing the upper and lower quartiles, the minimum and maximum values, and the presence or absence of outliers–extreme values that stand out from the normal data range. 

The following variables are represented and analyzed using boxplots:

**1. BMI**
   BMI values range from 18 to 42.2, with a median of 25.7 as represented by the orange line. The distribution of values is positively skewed, and there are three outlier values.

   Because the median falls beyond the healthy BMI range of 18.5 to 24.9, the middle value of the distribution qualifies as overweight. 186 respondents have a healthy weight. 2 respondents whose BMI are 18 and 18.1 fall into the underweight category, 155 respondents fall into the overweight category, and 99 respondents classify as obese. A majority of 256 values represent unhealthy weight, making 57.92% of the respondents have unhealthy BMI.

**2. BP**
   BP values range from 62 to 133, with a median of 93 as represented by the orange line. The distribution of values is positively skewed.

**3. Y**
   Y values range from 25 to 346, with a median of 140.5 as represented by the orange line. The distribution of values is positively skewed. 

**Task 3: Distribution of AGE, SEX, BMI and Y variables**
The provided findings depict the distributions of the variables AGE, SEX, BMI, and Y in a diabetic patient dataset.

**1. AGE Distribution:**
   The histogram depicts the age distribution of diabetic patients.It is inclined to the right, indicating a greater percentage of diabetic elderly patients.

**2. SEX Distribution:**
   The histogram depicts the gender distribution among diabetic patients (assuming binary encoding, 1.0 or 2.0, male or female). The percentage of diabetic males is significantly higher than diabetic females, the distribution is skewed towards diabetic males.

**3. BMI Distribution:**
   The histogram displays the distribution of Body Mass Index (BMI) among diabetes patients. The histogram depicts a symmetric curve with an essentially normal range of BMI around 18.9 to 24.9 for approximately 168 diabetic patients.While approximately 268 diabetic patients are within the range of an overweight value (25.0 and above).

**4. Y Distribution**
   The histogram depicts the distribution of the target variable Y, which could indicate a clinical result or a diabetes-related indicator.

**Task 4: Correlation of variables with disease progression**
A scatterplot is a graphical representation of correlations between a pair of variables. Correlations may be classified as negative or positive and linear or curved. Scatterplots also show the correlation strength of the two variables depending on how close or how far points scatter. 

**Age vs. Disease Progression**
These two variables do not have a clear correlation as points are not directed to any direction–upward (to the right) or downward (to the left). Hence, age and disease progression are neither positively or negatively correlated with each other. The wide scattering of values also indicates their weak correlation. It is unclear how diabetes progresses as age increases or decreases; there is no distinguishable structure (line or curve). 
	
**Body Mass Index vs. Disease Progression**
These two variables are positively correlated with each other; disease progression rate increases as BMI increases. Their correlation, however, is weak as points are not extremely close together. Outliers are also present. The shape of the scatterplot is linear rather than curved.
 
According to the Harvard School of Public Health, excess weight, especially obesity, harms almost every aspect of health, from reproductive and pulmonary function to memory and mood. Furthermore, obesity is linked to the following diseases:

1. Type 2 diabetes
2. Cardiovascular diseases like coronary artery disease and stroke
3. Numerous types of cancers like liver, kidney, breast cancer
4. Fertility issues and increased risk of miscarriages and gestational diabetes.
5. Respiratory diseases such as asthma, obstructive sleep apnea, and narrowed lung airways
6. Gallbladder diseases
7. Cognitive disorders like Alzheimer’s disease and dementia
8. Musculoskeletal problems like osteoarthritis, back pain, and disability
9. Mental health disorders like anxiety and depression

**Conclusion**
