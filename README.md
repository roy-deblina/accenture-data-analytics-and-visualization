# accenture-data-analytics-and-visualization

# Social Buzz Data Analysis and Visualization Project

## Introduction

As part of my Accenture Data Analysis and Visualization internship, I had the opportunity to work on a project for Social Buzz, a fast-growing technology unicorn. Social Buzz, a rapidly expanding social media platform with over 500 million monthly active users, produces more than 100,000 pieces of content daily. Given its massive scale and data-heavy operations, Social Buzz faced significant challenges in managing and leveraging its data effectively.

Accenture initiated a three-month Proof of Concept (POC) to assist Social Buzz in addressing these challenges and preparing for a successful Initial Public Offering (IPO). The focus was on three main tasks: auditing Social Buzz's big data practices, providing recommendations for a successful IPO, and analyzing the top five most popular categories of content on the platform.

## Problem Statement

Social Buzz required a comprehensive analysis to identify its top five most popular content categories. This analysis would help in understanding user preferences and guide content strategy. Additionally, the company needed insights into the number of unique content categories, the total number of reactions to the most popular category, and the month with the highest number of posts.

## Analysis Process

To address Social Buzz's requirements, the following steps were taken:

### Data Preparation

1. **Content Table**:
   - Deleted the URL column.
   - Removed quotation marks from category names.
   - Renamed the reaction column to reaction type.
   - Deleted the user ID column.

2. **Reaction Table**:
   - Deleted the user ID column.

### Data Merging

1. **Merge Reaction Table with Content Table**:
   - Added 'Type' and 'Category' columns to the Reaction Table using VLOOKUP to populate from the Content Table.

2. **Merge Resulting Table with Reaction Types Table**:
   - Added 'Sentiment' and 'Score' columns to the merged Reaction-Content Table using VLOOKUP to populate from the Reaction Types Table.

### Calculating Total Scores for Each Category

1. Created a new sheet listing unique categories from the merged table.
2. Used the SUMIF function to calculate the total scores for each category.

### Identifying the Top 5 Categories

1. Sorted the categories in descending order based on total scores.
2. Highlighted the top five categories from the sorted list.

### Additional Insights

1. **Unique Categories**: Counted the number of unique categories.
2. **Reactions to Most Popular Category**: Summed the reactions to the most popular category.
3. **Month with Most Posts**:
   - Extracted the month from the Datetime column.
   - Created a pivot table to count posts by month.

### Data Visualization

1. **Top 5 Content Categories (Bar Chart)**:
   - Created a pivot table with categories and count of content IDs.
   - Filtered and sorted to show the top five categories.
   - Inserted a bar chart.

2. **Sentiment Distribution (Pie Chart)**:
   - Created a pivot table with sentiment and count of content IDs.
   - Inserted a pie chart.

## Insights Found

Based on the analysis, the following insights were derived:

1. **Top 5 Content Categories**:
   - **Animals**: 1897 posts
   - **Science**: 1796 posts
   - **Healthy Eating**: 1717 posts
   - **Food**: 1699 posts
   - **Technology**: 1698 posts

2. **Unique Categories**: There are a total of 16 unique content categories.

3. **Reactions to the Most Popular Category**: The category 'Animals' had the highest engagement with 1897 reactions.

4. **Month with Most Posts**: The month of May showed the highest content engagement and the most reactions given.

## Conclusion

The analysis provided valuable insights into Social Buzz's content strategy. Identifying the top five content categories—Animals, Science, Healthy Eating, Food, and Technology—helps understand user preferences and guide future content creation. With 16 unique categories and high engagement in May, Social Buzz can leverage these insights to enhance user experience and optimize content delivery. This project not only supports Social Buzz in its scaling efforts but also prepares the company for a successful IPO by showcasing robust data-driven decision-making capabilities.

By effectively utilizing data analysis and visualization techniques, this project demonstrates the importance of data-driven strategies in managing and optimizing large-scale social media platforms.
