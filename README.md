# GroupDNA – WhatsApp Group Analytics

## 📌 Project Overview

**GroupDNA** is a Python-based WhatsApp Group Analytics project that analyzes a WhatsApp chat export and converts unstructured conversations into useful communication and activity insights.

The project reads a WhatsApp `.txt` chat file, identifies participants and messages, and performs different types of analysis such as message frequency, busiest day and hour, common words, activity patterns, response time, silent periods, and personality-based group archetypes.

The main purpose of GroupDNA is to demonstrate how **Python programming fundamentals and NumPy** can be used to process and analyze real-world text data.

---

## 🎯 Problem Statement

WhatsApp group conversations contain a large amount of unstructured information. Manually understanding who is most active, when the group is most active, which words are commonly used, and how participants communicate can be difficult.

GroupDNA provides a simple analytical solution by parsing a WhatsApp chat export and generating meaningful statistics and behavioral insights from the conversation.

---

## 🎯 Objectives

The main objectives of GroupDNA are:

* Parse WhatsApp chat data from a `.txt` file.
* Identify participants and calculate their message activity.
* Find the busiest day and busiest hour.
* Analyze frequently used words.
* Generate a participant-wise activity matrix using NumPy.
* Display activity patterns through a text-based heatmap.
* Calculate approximate response times.
* Identify silent days and silent streaks.
* Assign measurable personality archetypes based on communication patterns.
* Generate a final analytical report.

---

## 🛠️ Technologies Used

### Python

Python is used as the main programming language for:

* File handling
* String processing
* Data parsing
* Statistical calculations
* Dictionaries, lists and sets
* Functions and loops
* Date and time processing

### NumPy

NumPy is used for:

* Creating the activity matrix
* Performing numerical calculations
* Representing participant activity across 24 hours
* Generating the text-based activity heatmap

### Python Libraries

The project mainly uses:

```text
NumPy
datetime
```

The project does not require Pandas, Matplotlib, Seaborn, NLTK, or machine-learning libraries.

---

## 📂 Project Structure

```text
GroupDNA/
│
├── GroupDNA_Campus_Analytics.ipynb
├── campus_connect.txt
└── README.md
```

### Files

**GroupDNA_Campus_Analytics.ipynb**
Contains the complete Python implementation and analysis.

**campus_connect.txt**
Contains the sample WhatsApp-style conversation used as the input dataset.

**README.md**
Contains project documentation, objectives, methodology, and usage instructions.

---

## 📊 Dataset

The project uses a WhatsApp-style `.txt` conversation dataset named:

```text
campus_connect.txt
```

The dataset contains conversations between fictional participants:

* Aarav
* Meera
* Rohan
* Ananya
* Kabir

The dataset follows the standard WhatsApp exported-chat format:

```text
04/05/24, 09:15 - Aarav: Good morning everyone
04/05/24, 09:17 - Meera: Good morning!
```

A fictional dataset is used for demonstration and privacy protection.

The program can also be adapted to analyze a permitted WhatsApp chat export by changing the input file name.

---

## ⚙️ Methodology

The GroupDNA analysis follows these steps:

```text
WhatsApp TXT Dataset
        ↓
Read File
        ↓
Detect Date and Time
        ↓
Parse Messages
        ↓
Identify Participants
        ↓
Clean and Process Text
        ↓
Message Statistics
        ↓
Busiest Day & Hour
        ↓
Word Frequency Analysis
        ↓
NumPy Activity Matrix
        ↓
Activity Heatmap
        ↓
Response Time Analysis
        ↓
Silent Streak Analysis
        ↓
Personality Archetypes
        ↓
Final GroupDNA Report
```

---

## 🔍 Features

### 1. WhatsApp Chat Parser

The program reads the exported `.txt` file and separates:

* Date
* Time
* Sender
* Message content

It also handles multi-line messages using a simple timestamp-based parsing approach.

---

### 2. Group Overview

The project calculates:

* Total number of messages
* Number of participants
* Analysis period
* Messages sent by each participant
* Percentage of total activity
* Average message length

This provides an overview of the group's communication activity.

---

### 3. Busiest Day and Hour

The program analyzes timestamps to identify:

* Day with the highest number of messages
* Hour with the highest number of messages

This helps identify when group communication is most active.

---

### 4. Top Words

The project processes message text and counts frequently occurring words.

Common stop words such as:

```text
the
is
a
and
to
of
```

are removed so that more meaningful words can be identified.

The program displays the top words used in the group.

---

### 5. NumPy Activity Matrix

A **participant × hour** activity matrix is created using NumPy.

The matrix has the following structure:

```text
Participants × 24 Hours
```

For example:

```text
5 × 24
```

Each row represents a participant and each column represents an hour from `00` to `23`.

---

### 6. Activity Heatmap

The NumPy matrix is converted into a text-based heatmap.

Symbols represent different levels of activity:

```text
.  = No activity
░  = Low activity
█  = Higher activity
```

This provides a simple visual representation without requiring graphical libraries.

---

### 7. Response Time Analysis

The project calculates the approximate time between consecutive messages from different participants.

This provides an estimate of how quickly participants respond to ongoing conversations.

---

### 8. Silent Streak Analysis

For each participant, the program identifies:

* Number of silent days
* Consecutive inactive days
* Longest silent streak

This helps understand differences in participation patterns.

---

### 9. Personality Archetypes

GroupDNA assigns communication-based archetypes using measurable characteristics.

Examples include:

```text
THE SPAMMER
THE GROUP MOM
THE NIGHT OWL
THE STORYTELLER
THE DRAMA QUEEN
THE GHOST
THE COMEDIAN
THE QUESTION MASTER
```

The archetype is selected using activity patterns and message characteristics rather than manually assigning a label.

These archetypes are intended as **project-level analytical categories**, not psychological diagnoses.

---

## 💻 How to Run the Project

### Step 1 – Open Google Colab

Open Google Colab and create a new notebook.

### Step 2 – Upload the dataset

Upload:

```text
campus_connect.txt
```

using:

```python
from google.colab import files

uploaded = files.upload()
```

### Step 3 – Set the filename

The notebook uses:

```python
FILE_NAME = "campus_connect.txt"
```

### Step 4 – Run the notebook

Run all cells from top to bottom.

The notebook will generate the complete GroupDNA analysis.

---

## 📋 Expected Output

The final output contains:

```text
GROUPDNA – CAMPUS GROUP ANALYTICS

GROUP OVERVIEW
Total Messages
Participants
Analysis Period

MESSAGE COUNT
Participant-wise message statistics

ACTIVITY PEAK
Busiest Day
Busiest Hour

TOP WORDS
Frequently used words

NUMPY MATRIX
Participant × 24-hour activity matrix

RESPONSE TIME
Average response time

SILENT STREAKS
Inactive days and longest silent periods

PERSONALITY ARCHETYPES
Participant-wise analytical archetypes
```

---

## 🚧 Challenges

Some challenges addressed in the project include:

* Converting unstructured chat text into structured information.
* Detecting timestamps correctly.
* Separating sender names from message content.
* Handling messages containing punctuation.
* Processing different message frequencies.
* Comparing participants using measurable statistics.
* Representing hourly activity using a NumPy matrix.
* Avoiding unnecessary external libraries.

---

## 🔒 Privacy

The included dataset uses **fictional participant names and sample conversation data**.

Private WhatsApp conversations should not be uploaded to a public GitHub repository without appropriate permission.

If a real WhatsApp export is used for testing, it should remain private and should not be committed to a public repository.

---

## 🚀 Future Scope

GroupDNA can be extended in the future with:

* Support for more WhatsApp export formats.
* More advanced text analysis.
* Emoji analysis.
* Media-sharing statistics.
* Weekday and monthly activity analysis.
* Interactive dashboards.
* Sentiment analysis.
* Network-based conversation analysis.
* Database storage for larger datasets.
* Web-based visualization.

---

## 📚 Learning Outcomes

Through this project, the following concepts were practiced:

* Python file handling
* Lists and dictionaries
* Sets and tuples
* Loops and conditional statements
* Functions
* String manipulation
* Date and time processing
* Data cleaning
* Frequency analysis
* NumPy arrays
* Basic data analysis
* Real-world text-data processing

---

## 🤖 AI Assistance

AI tools were used as a development and learning aid for understanding programming concepts, improving code structure, debugging, and preparing project documentation.

The final implementation was tested and adapted for the project dataset.

---

## 👩‍💻 Project Information

**Project Name:** GroupDNA – WhatsApp Group Analytics

**Domain:** Python / Data Analysis

**Programming Language:** Python

**Main Library:** NumPy

**Dataset Type:** WhatsApp-style TXT conversation

**Execution Platform:** Google Colab / Jupyter Notebook

---

## 📌 Conclusion

GroupDNA demonstrates how a simple Python program can transform an unstructured WhatsApp conversation into meaningful analytical information. By combining file processing, string manipulation, statistical calculations, and NumPy-based analysis, the project provides insights into group activity, communication patterns, frequently used words, response behavior, silent periods, and participant archetypes.

The project also demonstrates the practical application of fundamental Python concepts to a real-world style dataset without relying on complex machine-learning frameworks or visualization libraries.
