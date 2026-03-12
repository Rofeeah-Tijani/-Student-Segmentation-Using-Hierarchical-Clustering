# -Student-Segmentation-Using-Hierarchical-Clustering

# 🎓 Student Segmentation Using Hierarchical Clustering

This project applies Hierarchical Clustering to identify distinct groups of students based on lifestyle, academic habits, and social behaviors. The goal is to uncover patterns that may influence academic performance and student behavior.

By grouping similar students together, we can better understand how factors such as study time, social activity, family background, and lifestyle choices relate to academic outcomes.

-----

**📌 Problem Statement**

Educational institutions often collect large amounts of student data, but identifying meaningful behavioral patterns from this data can be challenging.

The goal of this project is:

To use hierarchical clustering to identify distinct groups of students based on lifestyle, academic habits, and performance in order to understand patterns that influence academic outcomes.

Instead of analyzing students individually, clustering was used to discover natural groupings of students with similar characteristics.

These groups can help answer questions such as:

Are there groups of students with similar study behaviors?

Do lifestyle factors correlate with academic struggles?

Can we identify profiles of high-performing students?

---------

**📂 Dataset**

This project uses the Student Performance Dataset from the UCI Machine Learning Repository.

Dataset contains information about Portuguese secondary school students, including:

**Academic Factors**

study time

number of past failures

school support

family educational support

**Lifestyle Factors**

free time

going out with friends

alcohol consumption

romantic relationships

**Family & Background Factors**

parents' education

family relationships

internet access

travel time to school

---------

**⚙️ Methodology**

The analysis follows these main steps:

Data preprocessing

Feature encoding

Feature scaling

Hierarchical clustering

Cluster interpretation

Cluster visualization

**1️⃣ Data Preprocessing**

The dataset contains both numerical and categorical variables.

Since clustering algorithms operate on numerical data, categorical variables was converted into numerical form.

Example categorical variables:

school support (yes/no)

romantic relationship (yes/no)

internet access (yes/no)

extracurricular activities (yes/no)

--------

**2️⃣ Encoding Categorical Features**

Categorical variables were converted into numerical variables using One-Hot Encoding.

------

**Why One-Hot Encoding?**

Label encoding could incorrectly introduce ordinal relationships between categories.

-----

**3️⃣ Feature Standardization**

After encoding, the features were standardized using StandardScaler.

Why Standardization?

Clustering algorithms rely on distance calculations.

Features with larger numeric ranges (e.g., age vs failures) could dominate the clustering process.

**Standardization ensures:**

All variables have equal influence

Features are centered around mean = 0

Standard deviation becomes 1, which improves clustering accuracy.

**4️⃣ Hierarchical Clustering**

Hierarchical clustering was performed using Ward linkage.

Hierarchical clustering was chosen because:

It does not require specifying the number of clusters beforehand

It produces a dendrogram, which visually shows cluster structure

It helps identify natural groupings in the data

-----

**5️⃣ Dendrogram Analysis**

A dendrogram was used to visualize how clusters merge.

The dendrogram shows:

Vertical lines → clusters being merged

Height of merge → distance between clusters

To determine the number of clusters, a horizontal cut line was drawn.

The number of clusters is determined by counting the vertical branches intersected by the cut line.

This resulted in:

3 clusters

<img width="1129" height="746" alt="Screenshot (519)" src="https://github.com/user-attachments/assets/35683e02-a04f-4fd4-8deb-229d468373ff" />

------

**6️⃣ Assigning Cluster Labels**

After selecting the cluster threshold, cluster labels were generated.

-----

**📊 Cluster Profiling**

To understand the characteristics of each cluster, feature averages were computed which allows  to observe typical behavior patterns within each group.

----

**📈 Visualization of Cluster Profiles**

Cluster profiles were visualized using bar charts to compare feature averages across clusters.

This makes it easier to identify behavioral differences between groups.

<img width="1448" height="692" alt="Screenshot (518)" src="https://github.com/user-attachments/assets/8ceadbad-6aa0-4b21-8a48-09bce94ab472" />

-----

**🔍 Key Findings**

The clustering analysis revealed three distinct student profiles.

Cluster 1 – Less Academically Focused Students

Characteristics:

Higher number of academic failures

Lower parental education levels

More involvement in romantic relationships

Moderate study time

These students may face academic challenges or distractions that impact performance.

------

Cluster 2 – Highly Focused Students

Characteristics:

Highest study time

Very low academic failures

Higher parental education

Lower romantic involvement

This group appears to be the most academically serious students.

------

Cluster 3 – Moderately Focused Students

Characteristics:

Moderate study time

Moderate failure rates

Balanced social and academic behaviors

These students represent a middle group between highly focused and struggling students.

------


**💡 Insights**

The clustering analysis suggests that:

Parental education may influence academic focus

Study time strongly correlates with fewer failures

Lifestyle behaviors (e.g., romantic involvement) may influence academic performance

Students naturally form behavioral groups, not just individual variations

Understanding these patterns can help educators design targeted academic support strategies.

------

**🛠️ Tools Used**

Python libraries used in this project:

pandas

numpy

matplotlib

scikit-learn

scipy

-----

**📚 References**

UCI Machine Learning Repository
Student Performance Dataset

