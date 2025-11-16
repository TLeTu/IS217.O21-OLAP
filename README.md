# Steam Game Data Warehouse & BI Pipeline

This project is a comprehensive Business Intelligence solution built for the "Data Warehouse and OLAP" course at the University of Information Technology (VNU-HCM).

The primary goal is to build an end-to-end data warehouse for analyzing the **Steam game market**. The analysis focuses on key metrics like peak player counts, positive/negative reviews, and release trends, allowing for slicing and dicing by genre, publisher, and date.

The project uses the "Steam Releases" dataset from Kaggle, containing data on over 67,000 games released between 2006 and 2023.

Sources:
- Database: https://drive.google.com/drive/u/0/folders/1tnLzQccHgf707O6hKj5gElkaJEfBScM3
- Report: https://drive.google.com/drive/u/0/folders/1-iq0sYtr1zZaubdrlDjnLmSMntBR_9kG
- Demo videos: https://drive.google.com/drive/u/0/folders/1_tMSv_8IwWvGU68THbfTXsBJxvAcfNvt
- SSAS source code: https://drive.google.com/drive/u/0/folders/1nd2Tzwxq4rJYdNjbCHkv9ArHrQUaVCzU
- SSIS source code: https://drive.google.com/drive/u/0/folders/1mW4dGzcWDiB5mo85itDa2OcunocZuXVy
- Excel pivot: https://drive.google.com/drive/u/0/folders/1lPQyByU11cvHfjMNC6yPTR6M209jAUPH
- SSRS source code: https://drive.google.com/drive/u/0/folders/1DzIPeNsq1RiwJqYsCYnbhjob1zKaY6kt
- Data mining source code: https://drive.google.com/drive/u/0/folders/169f8LhccRZrK_gE7mTiLW7O6uYkt2sp5

This project utilizes the full Microsoft Business Intelligence stack:
* **Database:** SQL Server 2019
* **ETL (Extract, Transform, Load):** SQL Server Integration Services (**SSIS**)
* **OLAP Cube:** SQL Server Analysis Services (**SSAS**)
* **Query Language:** Multidimensional Expressions (**MDX**)
* **Reporting:** SQL Server Reporting Services (**SSRS**) & **Power BI**
* **Data Mining:** SSAS (Decision Trees)

## 🛠 Project Components

1.  **Data Integration (SSIS):** An SSIS package extracts data from the source .csv file, performs data conversions, removes duplicates, and loads the data into a star schema in the SQL Server data warehouse.
2.  **OLAP Cube (SSAS):** A multidimensional cube is built from the warehouse, complete with dimensions (Game, Publisher, Genre, Date) and measures (AllTimePeak, PositiveReviewCount, NegativeReviewCount). Hierarchies are created for time-based analysis (Year > Quarter > Month > Day).
3.  **Data Analysis (MDX):** The SSAS cube is queried directly using MDX and explored via Excel Pivot Tables to answer over 15 analytical questions, such as:
    * Top 10 games with the highest all-time peak players.
    * Top 5 genres with the most game releases per year.
    * Top 3 publishers by peak players per quarter.
4.  **Reporting (SSRS & Power BI):** Interactive reports and dashboards are created to visualize insights, including market trends over time and top games by genre.
5.  **Data Mining:** A separate module demonstrates data mining using the **Microsoft Decision Trees** algorithm on the "Stroke Prediction Dataset" to predict health outcomes based on patient attributes.
