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

SELECT 
    g.Name AS Genre, 
    SUM(il.Quantity) AS Tracks_Sold
FROM Genre g
JOIN Track t ON g.GenreId = t.GenreId
JOIN InvoiceLine il ON t.TrackId = il.TrackId
GROUP BY g.Name
ORDER BY Tracks_Sold DESC
LIMIT 5;
<img width="371" height="149" alt="image" src="https://github.com/user-attachments/assets/a24fa4ae-d5b4-41d3-85a7-94c60891866d" />

SELECT 
    c.FirstName, 
    c.LastName, 
    c.Country, 
    SUM(i.Total) AS Total_Spent
FROM Customer c
JOIN Invoice i ON c.CustomerId = i.CustomerId
GROUP BY c.CustomerId
ORDER BY Total_Spent DESC
LIMIT 5;
<img width="236" height="625" alt="image" src="https://github.com/user-attachments/assets/32fc2a93-0827-45c3-aa43-21896032f1f6" />

SELECT 
    BillingCountry, 
    SUM(Total) AS Total_Revenue
FROM Invoice
GROUP BY BillingCountry
ORDER BY Total_Revenue DESC
<img width="246" height="150" alt="image" src="https://github.com/user-attachments/assets/45382c1d-d260-4faa-8b68-2fbf67cbbb48" />

SELECT 
    ar.Name AS Artist, 
    SUM(il.UnitPrice * il.Quantity) AS Total_Revenue
FROM Artist ar
JOIN Album al ON ar.ArtistId = al.ArtistId
JOIN Track t ON al.AlbumId = t.AlbumId
JOIN InvoiceLine il ON t.TrackId = il.TrackId
GROUP BY ar.Name
ORDER BY Total_Revenue DESC
LIMIT 5;

<img width="208" height="149" alt="image" src="https://github.com/user-attachments/assets/4c290437-5fc1-4cd9-99b5-4eb5e6e1c438" />

SELECT 
    e.FirstName, 
    e.LastName, 
    e.Title, 
    SUM(i.Total) AS Total_Revenue_Generated
FROM Employee e
JOIN Customer c ON e.EmployeeId = c.SupportRepId
JOIN Invoice i ON c.CustomerId = i.CustomerId
GROUP BY e.EmployeeId
ORDER BY Total_Revenue_Generated DESC
LIMIT 3;
<img width="459" height="102" alt="image" src="https://github.com/user-attachments/assets/25aa7814-600b-4a86-8678-12da67817a87" />

