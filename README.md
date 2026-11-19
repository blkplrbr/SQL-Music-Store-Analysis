# SQL Business Analysis: Chinook Music Retailer

## Project Overview
This project simulates a consulting engagement with "Chinook Music," a digital media and retail store. The objective was to query the company's relational database to answer high-level business questions regarding customer value, regional sales, product profitability, and employee performance.

## The Business Problem
Chinook Music needed to optimize its marketing budget and licensing deals. Leadership required data-driven answers to identify their most valuable customers, profitable genres, and top-performing sales agents.

## Database Schema
The project utilizes the classic Chinook SQLite database, which includes tables for:
*   `Customer` (Names, Countries, Support Reps)
*   `Invoice` & `InvoiceLine` (Transaction data and total revenue)
*   `Track`, `Album`, `Artist`, and `Genre` (Product catalog)

## Business Questions Solved

1.  **Customer Value:** Identified the top 10 highest-spending customers and their countries to target a VIP loyalty program.
2.  **Regional Revenue:** Analyzed total revenue by billing country to identify the strongest global markets.
3.  **Product Profitability:** Found the top 5 most profitable music genres by total sales revenue to guide future licensing acquisitions.
4.  **Artist ROI:** Identified the highest-grossing artists and their total track sales volume to prioritize contract renegotiations.
5.  **Sales Performance:** Evaluated Sales Support Agents by calculating their total generated revenue and the number of customers they manage.

## SQL Skills Demonstrated
*   **Multi-Table Joins:** Connecting track and genre data to invoice line items.
*   **Aggregate Functions:** Utilizing `SUM()` and `COUNT()` to calculate total revenue and volume.
*   **Grouping & Filtering:** Using `GROUP BY` and `HAVING` clauses to segment data.
*   **Data Sorting:** Applying `ORDER BY DESC` and `LIMIT` to extract top-tier insights.

## Results

1. Top 5 Highest Spending customers

<img width="371" height="149" alt="image" src="https://github.com/user-attachments/assets/a24fa4ae-d5b4-41d3-85a7-94c60891866d" />

2. Revenue by country 

<img width="236" height="625" alt="image" src="https://github.com/user-attachments/assets/32fc2a93-0827-45c3-aa43-21896032f1f6" />

3. Top 5 Best Selling Genres

<img width="246" height="150" alt="image" src="https://github.com/user-attachments/assets/45382c1d-d260-4faa-8b68-2fbf67cbbb48" />

4. Top 5 Highest Grossing Artists


<img width="208" height="149" alt="image" src="https://github.com/user-attachments/assets/4c290437-5fc1-4cd9-99b5-4eb5e6e1c438" />

5Top Sales agents

<img width="459" height="102" alt="image" src="https://github.com/user-attachments/assets/25aa7814-600b-4a86-8678-12da67817a87" />

## Key Business Insights & Analysis

1. VIP Customer Targeting

The Data: The top 5 highest-spending customers are geographically diverse, with the highest spender (Helena Holý) located in the Czech Republic ($49.62), followed closely by Richard Cunningham in the USA ($47.62).

Business Action: Marketing should segment high-value customers by region for targeted, personalized outreach rather than relying on a generic global loyalty program.

2. Regional Revenue Drivers

The Data: The USA is the dominant market by a massive margin ($523.06), followed by Canada ($303.96) and France ($195.10).

Business Action: The USA, Canada, and France should receive the majority of localized ad spend. Emerging markets like India and Brazil are strong secondary targets for growth.

3. Genre Profitability (The "Rock" Factor)

The Data: Rock music is the undisputed king, selling 835 tracks—more than double the next closest genre (Latin at 386).

Business Action: The store should prioritize Rock inventory and featured playlists. Jazz, at the bottom (80 tracks), should be kept to a minimum to avoid dead stock.

4. Artist ROI (Who to promote)

The Data: Iron Maiden is the highest-grossing artist ($138.60), followed by U2, Metallica, and Led Zeppelin.

Business Action: Secure exclusive licensing or merchandising deals with these top artists. Feature them prominently on the homepage.

5. Sales Team Performance

The Data: Jane Peacock is the top-performing Sales Support Agent ($833.04), outperforming Margaret Park ($775.40) and Steve Johnson ($720.16).

Business Action: Jane's sales scripts and client management methods should be documented and used as the training template for the rest of the team.
