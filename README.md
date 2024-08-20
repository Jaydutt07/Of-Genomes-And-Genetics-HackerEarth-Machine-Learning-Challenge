# Of-Genomes-And-Genetics-HackerEarth-Machine-Learning-Challenge
## Predict the genetic disorders


#### Problem Statement
A genetic disorder is a health condition that is usually caused by mutations in DNA or changes in the number or overall structure of chromosomes. Several types of commonly-known diseases are related to hereditary gene mutations. Genetic testing aids patients in making important decisions in the prevention, treatment, or early detection of hereditary disorders.

With increasing population, studies have shown that there has been an exponential increase in the number of genetic disorders. Low awareness of the importance of genetic testing contributes to the increase in the incidence of hereditary disorders. Many children succumb to these disorders and it is extremely important that genetic testing be done during pregnancy.

#### Task

You are given a dataset that contains medical information of children who have genetic disorders. Predict the following:
- Genetic disorder 
- Disorder subclass

#### Data description

The dataset folder contains the following files:
- train.csv: 22083 x 45
- test.csv: 9465 x 43
- sample_submission.csv: 5 x 3

|Column name  | Description|
|-------------|-----------|
|Patient Id |Represents the unique identification number of a patient|
|Patient Age|Represents the age of a patient|
|Genes in mother's side|Represents a gene defect in a patient's mother|
|Inherited from father|Represents a gene defect in a patient's father|
|Maternal gene|Represents a gene defect in the patient's maternal side of the family|
|Paternal gene|Represents a gene defect in a patient's paternal side of the family|
|Blood cell count (mcL)|Represents the blood cell count of a patient|
|Patient First Name|Represents a patient's first name|
|Family Name|Represents a patient's family name or surname|
|Father's name|Represents a patient's father's name|
|Mother's age|Represents a patient's mother's name|
|Father's age|Represents a patient's father's age|
|Institute Name|Represents the medical institute where a patient was born|
|Location of Institute|Represents the location of the medical institute|
|Status|Represents whether a patient is deceased|
|Respiratory Rate (breaths/min)|Represents a patient's respiratory breathing rate|
|Heart Rate (rates/min)|Represents a patient's heart rate|
|Test 1 - Test 5|Represents different (masked) tests that were conducted on a patient|
|Parental consent|Represents whether a patient's parents approved the treatment plan|
|Follow-up|Represents a patient's level of risk (how intense their condition is)|
|Gender|Represents a patient's gender|
|Birth asphyxia|Represents whether a patient suffered from birth asphyxia|
|Autopsy shows birth defect (if applicable)|Represents whether a patient's autopsy showed any birth defects|
|Place of birth|Represents whether a patient was born in a medical institute or home|
|Folic acid details (peri-conceptional)|Represents the periconceptional folic acid supplementation details of a patient|
|H/O serious maternal illness|Represents an unexpected outcome of labor and delivery that resulted in significant short or long-term consequences to a patient's mother|
|H/O radiation exposure (x-ray)|Represents whether a patient has any radiation exposure history|
|H/O substance abuse|Represents whether a parent has a history of drug addiction|
|Assisted conception IVF/ART|Represents the type of treatment used for infertility|
|History of anomalies in previous pregnancies|Represents whether the mother had any anomalies in her previous pregnancies|
|No. of previous abortion|Represents the number of abortions that a mother had|
|Birth defects|Represents whether a patient has birth defects|
|White Blood cell count (thousand per microliter)|Represents a patient's white blood cell count|
|Blood test result|Represents a patient's blood test results|
|Symptom 1 - Symptom 5|Represents (masked) different types of symptoms that a patient had|
|Genetic Disorder|Represents the genetic disorder that a patient has|
|Disorder Subclass|Represents the subclass of the disorder|

#### Evaluation metric

##### Genetic Disorder
score1 = max(0, 100*metrics.f1_score(actual["Genetic Disorder"], predicted["Genetic Disorder"], average="macro"))

##### Disorder Subclass
score2 = max(0, 100*metrics.f1_score(actual["Disorder Subclass"], predicted["Disorder Subclass"], average="macro"))

##### Final score
score = (score1/2)+(score2/2)
