# Monthly-Assessment-Marks-Evaluation-Task-N8N
Automated n8n workflow to calculate students’ average marks and determine eligibility for placement drives at Innomatics Research Labs.

This repository contains an **n8n workflow** designed for **Innomatics Research Labs** to automate the process of calculating monthly assessment marks and determining student eligibility for the placement drive.

## 🎯 Objective

The goal of this workflow is to:
- Automate the process of evaluating student assessment marks.
- Compute the **average score** automatically.
- Generate an **eligibility result** based on performance.

## 🧠 Scenario Overview

Innomatics Research Labs conducts monthly assessments for students enrolled in **Data Analytics (DA)** and **Data Science (DS)** programs.  
To streamline evaluations, this n8n workflow:

1. **Collects marks** for each module using an integrated form.
2. **Calculates average marks** automatically.
3. **Checks eligibility** for the placement drive based on average performance.
4. **Displays a custom message** depending on the result.

## ⚙️ Workflow Logic

### 🧩 Workflow Nodes Overview
| Node Name | Purpose |
|------------|----------|
| **Eligibility Check for Placement Drive** | Captures student details and marks input. |
| **DA or DS Student?** | Determines the student stream (DA or DS). |
| **DA Marks** | Collects module marks for Data Analytics students. |
| **DS Marks** | Collects module marks for Data Science students. |
| **Data Analysis Average Calculation** | Calculates the average marks for DA modules. |
| **Data Science Average Calculation** | Calculates the average marks for DS modules. |
| **Checking Eligibility** | Compares average marks against the threshold (70). |
| **Eligible / Not Eligible** | Displays final status message. |


## 🧾 Eligibility Criteria

| Condition | Result |
|------------|---------|
| **Average > 70** | ✅ *Eligible for placement drive* |
| **Average ≤ 70** | ⚠️ *Not eligible — focus on improving weaker modules* |


## 🧮 Modules Considered

### 📊 Data Analytics (DA)
- Python  
- EDA  
- SQL  
- Power BI  
- Advanced Statistics  

### 🤖 Data Science (DS)
- Machine Learning (ML)  
- Artificial Neural Networks (ANN)  
- Convolutional Neural Networks (CNN)  
- Natural Language Processing (NLP)  
- Generative AI (GenAI)  


## 🧰 How It Works

1. **Collect Input via n8n Form**
   - The form accepts module-wise marks for either DA or DS students.

2. **Branch Decision (IF Node)**
   - Workflow identifies whether the student belongs to DA or DS stream.

3. **Average Calculation**
   - Uses Function Node to compute the mean of submitted marks.

4. **Eligibility Evaluation**
   - IF node checks if average > 70.

5. **Result Output**
   - Shows either:
     - 🎉 “You are eligible for the placement drive.”
     - ⚠️ “Not eligible — focus on improving your marks.”



## ▶️ Demo Video

🎥 *[Click here to watch the workflow in action](#)*  
https://www.linkedin.com/feed/update/urn:li:activity:7394019181249101825/

## 🧑‍💻 Setup Instructions

### 1. Clone the Repository
It's just a example: 
```bash
git clone https://github.com/<Ruchii151>/n8n-monthly-assessment.git
cd n8n-monthly-assessment

```
### 2. Import Workflow into n8n

Open your n8n instance.

Go to Workflows → Import from File.

Select monthly-assessment-eligibility.json.

Review connections and activate.

### 3. Test the Workflow

Execute the workflow.

Submit test responses through the n8n form.

Verify eligibility output


# 🪪 Author

Ruchita Patil
Email: pruchita565@gmail.com

LinkedIn Profile: www.linkedin.com/in/patil-ruchita
