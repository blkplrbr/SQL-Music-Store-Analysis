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

## Status
🚧 **Work in Progress:** The SQL scripts and visual outputs will be uploaded shortly.
