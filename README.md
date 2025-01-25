# Security Risk Evaluation via Log Analysis
- Tags: Machine Learning (Classification) , Class Imbalance, Log Analysis
- Language: Python
  
## Exploratory Data Analysis
The main goal of the project is to classify logs based on its risk level to secure services. The data comprises two columns: 'level' and 'full_log' features. The 'level' feature serves as a response variable, although its class distribution is highly imbalanced. The 'full_log' contains three types of data partitions (characters, numbers, special characters). Analyzing the word count across each level, we infer that the frequency of words in a log entry could indicate the log's level. However, some logs were identical across different levels.

## Prediction Model & Evaluation Metrics
A primary challenge is the high imbalance of the 'level' feature. To address this, an undersampling method was employed during the data preprocessing stage. By constructing datasets with three different proportions of undersampled data, we assessed the impact of the undersampling process. Moreover, tree-based models were preferred over the simple logistic regression approach due to the issue of multi-class classification, which is a known limitation of logistic regression. For tree- based methods, random forest and XGBoost were selected, catering to cybersecurity's need for rapid response. These methods can be executed in parallel, enabling quicker inference. Macro- recall was the main evaluation metric, given its importance in identifying hazardous attacks.

## Result and Error Analysis
Upon evaluating twelve models derived from three undersampled datasets and two learning methods, the process of undersampling notably enhanced model performance, achieving a macro- recall value of 0.997. However, the lack of industry-specific knowledge posed significant challenges, making assumptions difficult and sensitive tasks, like outlier handling, more complex. In the future, incorporating model selection based on inference time could lead to better model identification, crucial for the fast-paced nature of cybersecurity. Additionally, exploring online learning algorithms might offer valuable improvements.
