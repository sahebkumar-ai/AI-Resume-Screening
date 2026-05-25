# Resume-Screening
# Introduction
AI Resume Screening is a tool that uses artificial intelligence to automate the process of resume screening and shortlisting. The tool uses natural language processing and machine learning algorithms to analyze resumes and classify them to the job roles based on the words in their resume.

Our tool will be designed to make the hiring process easier for both HR teams and job seekers. Our idea is to develop a user-friendly web page that enables HR teams to select the specific job role they are recruiting for. Once the job role is chosen, a link is shared with potential candidates who can then upload their resumes.

Using pre-trained machine learning models, which are trained on thousands of resumes , our tool automatically filters out resumes that do not match the job requirements. Resumes are categorized based on specific keywords and phrases related to the job role ( for example , python developer – main words can be python , developed , project , computer science etc). If a candidate's resume matches the job description, they are immediately notified and their resume is uploaded to the company's database. Even if a candidate’s resume doesn’t match the description , it shows the potential role which is suitable for the uploaded resume.

Our tool saves HR teams valuable time and energy as they no longer need to manually sift through hundreds of resumes. Job seekers also benefit from receiving immediate feedback on their eligibility, streamlining their job search process.

# Features
Automated resume screening: AI Resume Screening saves time and effort by automatically screening resumes based on job requirements and pre-defined criteria.

Improved accuracy: The tool uses advanced algorithms to analyze resumes, reducing the likelihood of human bias and improving the accuracy of the shortlisting process. We have achieved 91 percent accuracy.

Efficient process: Each resume is categorized with the model in less than 5 seconds.

Detailed output : The HR gets a detailed output of the Name, Email, Location, and the candidate's resumé, based on the scores.

# Usage
The code consists of the following parts:

Upload_Resume.py : This is the code which integrates the UI with the Trained model. Use the command “streamlit run Upload_Resume.py” which opens the web browser where the candidate can upload the resume. Alternatively the code can be hosted online using streamlit and the link can directly be sent to the candidate,to upload the resume.

model_training.ipynb : It is the jupyter notebook which we used to train the final model on all algorithms. It also contains the accuracies of each algorithm we have used.TF-IDF was used to extract the features from the pre-processed resume.

cv.pickle : It is the pickled file which contains the features of the model trained on the resumes by using TF-IDF. This pickle file is used to compare the features of the Uploaded resume with the model.

RF.joblib.zip: It contains the compressed machine learning model (Random Forest) which had the highest accuracy. This is the model used to predict the category in which the resume fits. Decompress this file to get the pretrained model 'RF.joblib'

SQL.txt : Contains the MySQL queries to set up a database to store the details of the short listed candidates.

HR.py: The page where HR enters the job role which is open for hiring, based on which shortlisting of candidates is done. Use the command “streamlit run HR.py” to run it in the local server.

pages/Show_Resumes.py: It displays the resumes of the shortlisted candidates by sorting them in descending order of the scores.

# Other things to know:
The data of shortlisted candidates will be stored in a MySQL database, making it feasible to view their profiles.

The 'pages' folder should be placed in the same parent folder which contains 'HR.py' and 'Show Resumes.py' shouldn't be moved out of 'pages'

# Datasets used for the model:
https://www.kaggle.com/datasets/gauravduttakiit/resume-dataset

https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset


# 🤖 AI Resume Screening System

An intelligent AI-powered Resume Screening and Candidate Shortlisting System built using **Machine Learning**, **Natural Language Processing (NLP)**, **Streamlit**, and **MySQL**.

The system automatically analyzes resumes, predicts candidate job categories, calculates skill-match scores, stores shortlisted resumes in a database, and enables HR teams to manage applicants efficiently.

---

# 🚀 Features

- ✅ AI-based Resume Classification
- ✅ Automatic Resume Screening
- ✅ Skill Matching Score Calculation
- ✅ Resume Upload Support (PDF, DOCX, TXT)
- ✅ NLP-based Resume Cleaning
- ✅ Candidate Shortlisting
- ✅ Email Notification System
- ✅ Resume Viewer Dashboard
- ✅ MySQL Database Integration
- ✅ Streamlit Web Interface

---

# 🧠 Machine Learning & NLP

This project uses:

- **TF-IDF Vectorization**
- **Random Forest Classifier**
- **Natural Language Processing**
- **Text Cleaning & Stopword Removal**
- **Resume Category Prediction**

---

# 📌 Supported Resume Categories

| Category |
|----------|
| Accountant |
| Advocate |
| Agriculture |
| Apparel |
| Arts |
| Automobile |
| Aviation |
| Banking |
| BPO |
| Business Development |
| Chef |
| Consultant |
| Data Science |
| DevOps Engineer |
| DotNet Developer |
| Electrical Engineering |
| Finance |
| Healthcare |
| HR |
| Information Technology |
| Java Developer |
| Mechanical Engineer |
| Network Security Engineer |
| Python Developer |
| Sales |
| SAP Developer |
| Teacher |
| Testing |
| Web Designing |
| And More... |

---

# 📂 Project Structure

```bash
AI-Resume-Screening-System/
│
├── app.py
├── screening.py
├── dashboard.py
├── train_model.py
│
├── models/
│   ├── RF.joblib
│   └── cv.pickle
│
├── dataset/
│   └── resumes.csv
│
├── uploads/
├── requirements.txt
└── README.md
```

---

# ⚙️ Installation

## 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/ai-resume-screening-system.git
cd ai-resume-screening-system
```

---

## 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux/Mac

```bash
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install streamlit
pip install pandas
pip install numpy
pip install scikit-learn
pip install mysql-connector-python
pip install nltk
pip install joblib
pip install PyPDF2
pip install docx2txt
pip install keras
pip install matplotlib
```

---



# 📥 Resume Upload & Screening

The system accepts:

- PDF Files
- DOCX Files
- TXT Files

Supported operations:

- Resume Parsing
- Text Extraction
- Resume Cleaning
- Skill Matching
- Category Prediction

---

# 🧹 Resume Cleaning Process

The uploaded resume undergoes:

- Lowercase conversion
- Special character removal
- Stopword removal
- Text normalization
- Whitespace cleaning

---

# 🏋️ Model Training

The model is trained using:

- TF-IDF Vectorizer
- Random Forest Classifier

### Example Training Pipeline

```python
cv = TfidfVectorizer(max_features=20000)

model = RandomForestClassifier()

model.fit(X_train, y_train)
```

---

# 📊 Skill Matching Algorithm

The system compares:

- HR required skills
- Resume content keywords

Then calculates a matching percentage score.

Example:

```text
Python, SQL, Machine Learning
```

Resume score is calculated based on keyword matches.

---

# 📧 Email Notification System

Shortlisted candidates receive automated email notifications.

### Environment Variables

```env
SENDER_ADDRESS=your_email@gmail.com
SENDER_PASSWORD=your_password
SMTP_SERVER_ADDRESS=smtp.gmail.com
PORT=587
```

---

# 🖥️ Run Streamlit Application

Start the Streamlit server:

```bash
streamlit run app.py
```

---

# 🔍 Resume Dashboard

HR can:

- View candidate resumes
- Download resumes
- Sort by score
- Filter shortlisted candidates
- Open resumes directly in browser

---

# 📈 Workflow

```text
Resume Upload
       ↓
Text Extraction
       ↓
Resume Cleaning
       ↓
TF-IDF Vectorization
       ↓
ML Prediction
       ↓
Skill Matching
       ↓
Candidate Shortlisting
       ↓
Email Notification
```

---

# 🛠️ Technologies Used

- Python
- Streamlit
- Scikit-learn
- Random Forest
- TF-IDF
- NLP
- MySQL
- Keras
- NLTK
- Pandas
- NumPy

---

# 📊 Machine Learning Models

Implemented algorithms include:

- Random Forest Classifier
- Naive Bayes
- SVM
- KNN
- AdaBoost

---

# 🌍 Applications

- HR Automation
- Resume Filtering
- Candidate Ranking
- Recruitment Management
- AI Hiring Systems

---

# 📈 Future Improvements

- Resume Ranking Dashboard
- GPT-based Resume Analysis
- OCR Resume Parsing
- Cloud Deployment
- Multi-language Resume Support
- Real-Time Analytics
- Admin Authentication System

---


