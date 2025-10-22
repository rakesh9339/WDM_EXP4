### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```python
# Visitor segmentation based on characteristics
# read the data

import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('/clustervisitor (2).csv')


# Perform segmentation based on characteristics (e.g., age groups)

age_group_conditions = {
    '18-25': (df['Age'] >= 18) & (df['Age'] <= 25),
    '26-35': (df['Age'] >= 26) & (df['Age'] <= 35),
    '36-45': (df['Age'] >= 36) & (df['Age'] <= 45),
    '46-55': (df['Age'] >= 46) & (df['Age'] <= 55),
    '55+': (df['Age'] > 55)
}


#Plot

import matplotlib.pyplot as plt

plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()


```

### Output:
## Age_group_conditions Output:
<img width="579" height="633" alt="image" src="https://github.com/user-attachments/assets/04f19850-0bcb-42f5-990d-2176eb39e104" />
## Visual Plot:
<img width="835" height="645" alt="image" src="https://github.com/user-attachments/assets/ee433bdc-59e7-48e9-bc22-cff108e08d5e" />


### Visualization:
```python
# Create a list to store counts of visitors in each age group

visitor_counts = []

# Count visitors in each age group



for group, condition in age_group_conditions.items():
    count = df[condition].shape[0]
    visitor_counts.append(count)

age_group_labels = list(age_group_conditions.keys())
    
# Define age group labels and plot a bar chart

import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(10, 7))
sns.scatterplot(x='Age', y='Salary', hue='Cluster', data=df_salary, palette='viridis', s=100)
plt.title('Visitor Clusters based on Age and Salary')
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()
```
### Output:
<img width="845" height="589" alt="image" src="https://github.com/user-attachments/assets/b10bd80e-8ba7-4d73-af85-3f5809aca4bc" />


### Result:
 Thus the  Cluster and Visitor Segmentation for Navigation patterns in Python implemented successfully
