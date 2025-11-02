# 🎬 Netflix Dashboard – Data Analysis & Visualization Project  

<img width="750" height="512" alt="Netflix-Logo" src="https://github.com/user-attachments/assets/dc68a0c5-0587-4027-a8db-e51a06438b8f" />

---

## 📝 Introduction  

**Project on Netflix Data Analysis** — I imported the raw dataset into **VS Code** and cleaned it using **Python**, handling missing values, standardizing columns, and removing duplicates.  
After preprocessing, I exported the cleaned data and imported it into **Power BI** to build an interactive dashboard with KPIs, trend indicators, and Netflix-themed visuals that explore:  
- Content distribution  
- Top genres  
- Release year trends  
- Country-level insights  

---

## ⚙️ Tools Used  

| Category | Tools / Technologies |
|-----------|----------------------|
| **Programming Language** | Python |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn |
| **Data Visualization & BI** | Power BI |
| **Development Environment** | VS Code, Jupyter Notebook |
| **Dataset** | Netflix Titles (Movies & TV Shows) |

---

## 🧠 Libraries Used  

<img width="479" height="104" alt="Python Libraries" src="https://github.com/user-attachments/assets/592a7415-70aa-4ea0-8b8b-5a061c5ec59e" />

- **Pandas:** A powerful data analysis library used for cleaning, organizing, and transforming the Netflix dataset. It helped handle missing values, remove duplicates, and perform data exploration efficiently using DataFrames.  

- **NumPy:** A numerical computing library that provided fast operations on large datasets. It was mainly used for performing mathematical calculations and converting duration data into minutes.  

- **Matplotlib:** A visualization library used to create informative charts such as pie and bar graphs. It helped in visually representing key insights like content type distribution, top countries, and overall trends in Netflix data.  

---

## 📥 Data Loading  

The dataset was imported directly from an online source using **Pandas**.  
It was accessed from the **TidyTuesday GitHub repository**, which provides weekly datasets for data analysis practice.  

<img width="1147" height="91" alt="Screenshot 2025-11-02 150724" src="https://github.com/user-attachments/assets/83b0e547-945c-42f7-9778-40db614d5ada" />

### 🔍 Data Preview  

<img width="273" height="120" alt="Screenshot 2025-11-02 151359" src="https://github.com/user-attachments/assets/6bbc61b0-fd96-454c-b493-6306356c56ce" />

To get an initial look at the dataset, the `df.head()` function was used.  
This command displays the **first five rows** of the DataFrame, allowing us to quickly understand the structure of the data — such as column names, data types, and sample values.

<img width="1415" height="568" alt="Screenshot 2025-11-02 151548" src="https://github.com/user-attachments/assets/7ada6134-7ba5-4dd9-b181-bb14c711d052" />

### 📊 Statistical Summary 

<img width="240" height="104" alt="Screenshot 2025-11-02 151843" src="https://github.com/user-attachments/assets/033e74fc-2b49-4c4a-8254-ba1669e186f7" />

The `df.describe()` function was used to generate a **statistical summary** of the numerical columns in the dataset.  
It provides key insights such as **count, mean, minimum, maximum, and standard deviation**, helping to understand the data’s overall distribution and detect any anomalies.


<img width="289" height="325" alt="Screenshot 2025-11-02 151851" src="https://github.com/user-attachments/assets/e9c1ab6d-66d1-4f3f-906e-a73fab1b897a" />

### 📐 Dataset Dimensions  

The `df.shape` attribute was used to check the **dimensions of the dataset** — specifically, the number of **rows** and **columns** it contains.

<img width="257" height="150" alt="Screenshot 2025-11-02 152553" src="https://github.com/user-attachments/assets/f8d40e48-1018-4fa1-a579-1a6e11c2a399" />

### 🧾 Data Information  

The `df.info()` function was used to display a concise summary of the dataset, including **column names**, **data types**, and the **number of non-null values** in each column.

<img width="464" height="562" alt="Screenshot 2025-11-02 152803" src="https://github.com/user-attachments/assets/32b30860-db38-44a1-b8f3-b61b7b5b056e" />

### 🚫 Missing Values Check  

The `df.isnull().sum()` function was used to identify the **total number of missing (null) values** in each column of the dataset.

<img width="327" height="460" alt="Screenshot 2025-11-02 152854" src="https://github.com/user-attachments/assets/386c6e92-c4e1-427e-9422-d77ff754537d" />

### 🔁 Duplicate Records Check  

The `df.duplicated()` function was used to detect **duplicate rows** in the dataset.  
When combined with the `.sum()` method, it returns the **total count of duplicate entries**.

<img width="578" height="120" alt="Screenshot 2025-11-02 152959" src="https://github.com/user-attachments/assets/b4a464db-05da-426e-858d-d8d0b3c9a12f" />

### 🧩 Data Types Check  

The `df.dtypes` attribute was used to display the **data type** of each column in the dataset.  
This helps understand whether a column contains numerical, categorical, or text data — which is essential for choosing the right cleaning and visualization techniques.

<img width="351" height="496" alt="Screenshot 2025-11-02 153131" src="https://github.com/user-attachments/assets/5e508bfa-2a42-454b-b250-b1165b66d843" />

### 🧼 Handling Missing Values  

To maintain data quality, rows with missing values in critical columns like **`date_added`** and **`rating`** were removed using the `dropna()` function.

<img width="616" height="106" alt="Screenshot 2025-11-02 153644" src="https://github.com/user-attachments/assets/f331fab0-aa8e-4037-ac4f-d765ddb6c1c6" />

Checking data after removing the missing values 

<img width="306" height="422" alt="Screenshot 2025-11-02 153837" src="https://github.com/user-attachments/assets/c6e7fbd9-c14a-40ff-a1d2-028fc788eff5" />

### 🌍 Handling Missing Country Data  

To handle missing values in the **`country`** column, the most frequently occurring country (mode) was used to fill the gaps. This helps maintain dataset consistency without losing valuable records.

<img width="880" height="88" alt="Screenshot 2025-11-02 154823" src="https://github.com/user-attachments/assets/5bf7c60d-8821-4279-8412-01914b01ea4f" />

After cleaning all the data

<img width="393" height="604" alt="Screenshot 2025-11-02 154928" src="https://github.com/user-attachments/assets/ba5769c7-bc05-44c8-9032-36c421a0aa14" />

### ⏱️ Converting Duration into Minutes  

<img width="722" height="720" alt="Screenshot 2025-11-02 155229" src="https://github.com/user-attachments/assets/8a3e6265-2a9f-4489-b940-fe5638c36523" />

The dataset contains a `duration` column with mixed formats — some entries represent **movies** in minutes (e.g., *"90 min"*) and others represent **TV shows** in seasons (e.g., *"2 Seasons"*).  

To make this data consistent and comparable, a custom function `convert_to_minutes()` was created to standardize all durations into minutes:  

<img width="453" height="421" alt="Screenshot 2025-11-02 155241" src="https://github.com/user-attachments/assets/049377ba-c155-40f7-8707-c1303e2b57bf" />

### 💾 Exporting the Cleaned Dataset  

After cleaning, transforming, and standardizing the data, the final version of the dataset was exported as a **CSV file** for further visualization and analysis in **Power BI**.

<img width="523" height="128" alt="Screenshot 2025-11-02 155338" src="https://github.com/user-attachments/assets/5a97f72c-1cda-4d73-aa1f-ae7a931f816d" />

## 📊 Power BI Dashboard – Netflix Content Insights  

![Netflix Dashboard_page-0001](https://github.com/user-attachments/assets/237c0791-affc-4762-b95c-2588ba91a23d)

### 🎯 Objective  
The main goal of this Power BI dashboard is to explore and visualize Netflix’s extensive content library, providing clear insights into trends across movies, TV shows, genres, directors, and countries.  
After cleaning and preparing the dataset in Python, the processed data was imported into Power BI to build a dynamic and interactive dashboard with a **Netflix-inspired red and black theme**.  

### 🧩 Dashboard Overview  
The dashboard provides an at-a-glance view of Netflix’s global content data through KPIs, visual charts, and trend indicators.  
It highlights the overall structure of Netflix’s content in terms of type, duration, geography, and release year.  

**Key Performance Indicators (KPIs):**  
- **Total Titles:** 7,768 — representing all the shows and movies combined.  
- **Total Movies:** 5,371 — making up the majority of Netflix’s catalog.  
- **Total TV Shows:** 2,397 — showing Netflix’s growing investment in serial content.  
- **Total Directors:** 4,045 — unique directors contributing to the platform’s creative diversity.  
- **Total Countries:** 682 — illustrating Netflix’s vast global footprint.  

### 📈 Visual Breakdown & Insights  

#### 🔹 Longest Series (Minutes)
A horizontal bar chart visualizes the longest-running TV series on Netflix based on total duration. Shows like *Grey’s Anatomy*, *NCIS*, and *Supernatural* dominate the list, each with thousands of minutes of total runtime.  
This visualization helps identify content that has maintained long-term viewer engagement.

#### 🔹 Top 10 Countries of Shows  
A treemap visualization shows the top-producing countries on Netflix.  
The **United States** leads by a wide margin, followed by **India**, **United Kingdom**, and **Japan**.  
This highlights how Netflix’s content library is primarily dominated by North American productions but is steadily diversifying with contributions from Asia and Europe.

#### 🔹 Show vs Year  
A line chart showing the count of new shows released each year.  
The data reveals a noticeable growth in Netflix’s content releases from 2010 to 2020, with a sharp peak between 2018 and 2020, reflecting the streaming boom during that period.  
This visualization helps understand production trends and content expansion over time.

#### 🔹 Movies vs TV Shows  
A donut chart compares the proportion of **Movies (69%)** to **TV Shows (31%)**.  
This insight confirms that Netflix’s library is still heavily dominated by movies, even as the platform continues to push original TV content.

#### 🔹 Genre vs Show  
A bar chart showcasing the top genres available on Netflix.  
The most popular categories include **Documentaries**, **Stand-Up Comedy**, **Dramas**, and **Children & Family Movies**.  
This visualization helps understand what types of content Netflix focuses on and what genres attract the most production activity.

### 🎨 Dashboard Theme & Design  
- The dashboard follows a **Netflix-inspired color palette** of **red, black, and white**, designed to replicate the platform’s signature look.  
- Clean typography, bold KPIs, and minimal borders enhance readability.  
- Trend indicators and data labels are added for better interpretation.  
- Background visuals of Netflix posters are used for an immersive viewing experience.  

### 💡 Conclusion  
This dashboard effectively summarizes Netflix’s global content landscape, providing a comprehensive overview of its production trends, genre distribution, and regional diversity.  
It combines data cleaning in Python and interactive visualization in Power BI to transform raw data into meaningful business insights.  

✅ *This project demonstrates end-to-end data analysis skills — from Python-based data preparation to advanced Power BI dashboard design.*

