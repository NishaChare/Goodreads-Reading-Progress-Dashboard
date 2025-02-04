# Goodreads-Reading-Progress-Dashboard
Welcome to the Goodreads Reading Progress Dashboard project! This interactive Power BI dashboard helps you track and analyze your reading habits using data exported from Goodreads. Whether you're a book lover, a data enthusiast, or both, this project provides valuable insights into your reading journey.

Table of Contents

Project Overview
This project is a Power BI dashboard that visualizes and analyzes reading data exported from Goodreads. It provides insights into reading habits, such as:
Books read per month/year.
Pages read over time.
Genre and author preferences.
Reading speed and progress toward annual goals.
The dashboard is designed to be interactive, allowing users to filter data by genre, author, month, rating, and more.

Features
Interactive Slicers: Filter data by genre, author, month, rating, and reading status.
Key Metrics: Track books read, pages read, reading speed, and goal progress.
Visualizations: Bar charts, line charts, treemaps, and card visuals for easy data exploration.
Insights: Discover your most-read genres, highest-rated books, and reading trends over time.

Dataset
The dataset used in this project is exported from Goodreads. It typically includes the following columns:
Title: Name of the book.
Author: Author of the book.
Genre: Genre/category of the book.
Pages: Number of pages.
Start Date: When you started reading the book.
End Date: When you finished reading the book.
Rating: Your rating (e.g., 1-5 stars).
Reading Status: Read, Currently Reading, or To Read.

Tools and Technologies
Power BI: For data visualization and dashboard creation.
DAX (Data Analysis Expressions): For advanced calculations and metrics.
Goodreads: Source of the dataset (exported as CSV).
Power Query: For data cleaning and transformation (optional).

How to Use
Export Data from Goodreads:
Go to your Goodreads account and export your library data as a CSV file.
Load Data into Power BI:
Open Power BI Desktop.
Click on Get Data and import the CSV file.

Build the Dashboard:

Use the provided DAX formulas and visualizations to create the dashboard.
Customize the layout and visuals as needed.
Interact with the Dashboard:
Use slicers to filter data dynamically.
Explore insights like reading speed, genre preferences, and goal progress.

Key Metrics and Visualizations
Metrics:
Books Read: Total number of books read.
Pages Read: Total number of pages read.
Reading Speed: Average pages read per hour (PPH).
Goal Progress: Progress toward your annual reading goal.

Visualizations:
Bar Chart: Books read per month.
Line Chart: Pages read over time.
Treemap: Genre distribution.
Card Visuals: Key metrics like total books read and average rating.

DAX Formulas
Here are some key DAX formulas used in the project:

Total Books Read:
Total Books Read = COUNTROWS('year_wise_clean_data')

Total Pages Read:
Total Pages Read = SUM('year_wise_clean_data'[Number of Pages])

reading_duration:
reading_duration = DATEDIFF(year_wise_clean_data[Starting Date],year_wise_clean_data[End Date],DAY)

Reading_Speed
Reading_Speed = DIVIDE(SUM('year_wise_clean_data'[Number of Pages]), SUM('year_wise_clean_data'[reading_duration]))

no.of books read
no.of books read = DISTINCTCOUNT(year_wise_clean_data[Author])

Average_myRating
Average_myRating = AVERAGE('year_wise_clean_data'[My Rating])

Thank you for checking out my Goodreads Reading Progress Dashboard! If you have any questions or feedback, feel free to reach out. Happy reading! 📖✨






