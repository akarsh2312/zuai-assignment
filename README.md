# 🧮 IB Math IA & EE Scraping and Data Storage Application  

## 🎯 Objective  
This project is designed to scrape IB Math AI SL IA (Internal Assessment) and EE (Extended Essay) samples from the Nailib website. The extracted data is cleaned and stored in a MongoDB database, ensuring easy access for further analysis and processing.  

---

## 🚀 Key Features  

### 🔍 Data Extraction  
Efficiently scrapes key information from sample pages, including:  
- **Title**: The name of the IA or EE.  
- **Subject**: Example: Math AI SL.  
- **Description**: Extracts checklists or instructions.  
- **Sections**: Gathers detailed content under sections such as:  
  - *Introduction*, *Mathematical Information*, etc.  
- **Word Count**: Extracted word count of the content.  
- **Read Time**: Estimated time required to read the document.  
- **File Link**: Links to downloadable resources if available.  
- **Publication Date**: Captures and stores the date of publication (if provided).  

### 🛠️ Data Processing & Storage  
- **Data Cleaning**: Automatically removes extra spaces, handles missing fields, and ensures consistency.  
- **MongoDB Integration**:  
  - Utilizes MongoDB for secure and structured data storage.  
  - Employs **upsert functionality** to avoid duplicate entries.  

### ⚙️ Error Handling  
Gracefully handles challenges like:  
- Network failures.  
- Missing or incomplete data on scraped pages.  

### 🌟 Optional Enhancements  
- **Automation**: Set up periodic scraping using **Cron Jobs**.  
- **REST API**: Provides an API to access the stored data.  
- **Dockerized Setup**: Simplifies deployment through containerization.  

---

## 🛠️ Technologies Used  

- **Python**: Core language for scripting and backend logic.  
- **Libraries**:  
  - **BeautifulSoup** or **Selenium** for web scraping.  
  - **PyMongo** for MongoDB database operations.  
- **MongoDB**: Primary database for storing extracted data.  
- **Docker**: For optional containerization and deployment.  
- **Cron**: Automates periodic execution of the scraper.  

---

## 📜 Project Setup  

### 🖥️ Prerequisites  
1. **Python 3.x** and **pip** (Python package installer).  
2. **MongoDB** installed locally or accessed via a cloud service.  

### ⚡ Steps to Run the Project  

1. **Clone the repository**:  
   ```bash  
   git clone https://github.com/akarsh2312/zuai-assignment  
   cd document-capture-scraping  


2. **Install Dependencies**:  
Navigate to the project directory and install the required Python libraries and modules:  
```bash  
pip install -r requirements.txt  

3. **Run the backend**:
```bash 
python app.py
(Optional) If you want to view the scraped data in a frontend React app:

4. **Build and run the Docker container**:
```bash 
docker build -t document-capture-scraping .
docker run -p 5000:5000 document-capture-scraping

### How It Works

- **Scraping**: Scrapes IB Math IA SL and EE data from Nailib.
- **Data Cleaning**: Ensures the extracted data is formatted properly.
- **MongoDB Storage**: Stores the data in MongoDB, preventing duplicates.
- **API Access**: Exposes a REST API to query and retrieve the data.
- **Automation**: Sets up Cron to run the scraper at intervals for updated data.