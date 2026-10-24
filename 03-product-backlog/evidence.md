# Product Backlog Evidence

This page presents the documented Product Catalogue backlog for **D6 Food Bulk**, including its user story, task categories, Tiyani Ngwana's assigned contributions, Trello records, and supporting database and interface evidence. Each screenshot can be selected to open at full resolution.

## 1. Product Catalogue Backlog

### 1.1 User Story

> **As a student, I want to browse and search for grocery products so that I can easily find the items I need.**

### 1.2 Backlog Objective

Provide a clear, searchable catalogue that displays grocery information, categories, availability and discounted student prices.

### 1.3 Backlog Items

#### 1.3.1 Catalogue Design

- Design the Product Catalogue page.
- Design the Product Details page.
- Design the Product Catalogue interface.
- Create grocery categories.

#### 1.3.2 Product Data and Integration

- Design the product database.
- Add grocery products and categories to the database.
- Connect the catalogue to the database.
- Display product images and descriptions.

#### 1.3.3 Search and Discovery

- Implement product search.
- Implement category filtering.
- Allow students to browse products efficiently.

#### 1.3.4 Student Pricing and Availability

- Display student discount prices.
- Display product availability.
- Keep catalogue information clear enough to support purchasing decisions.

#### 1.3.5 Testing and Review

- Test product browsing.
- Test search and filter functionality.
- Test catalogue loading performance.
- Fix identified bugs and review the completed work.

### 1.4 My Assigned Contribution

The Trello checklists assign the following Product Catalogue tasks to **Tiyani Ngwana**:

- Design the product database.
- Connect the catalogue to the database.
- Display student discount prices.
- Display product availability.
- Test catalogue loading performance.
- Fix bugs and support the final review.

## 2. Screenshot Evidence

The screenshots document the Product Catalogue user story and checklist items organised across four working days.

<p align="left">
  <a href="../assets/product-backlog/product_catalogue_day_1.png"><img src="../assets/product-backlog/product_catalogue_day_1.png" alt="Product Catalogue Day 1 design and database checklist" width="46%"></a>
  <a href="../assets/product-backlog/product_catalogue_day_2.png"><img src="../assets/product-backlog/product_catalogue_day_2.png" alt="Product Catalogue Day 2 development and database connection checklist" width="46%"></a>
</p>

<p align="left"><sub><strong>Figures 1–2.</strong> Day 1 documents catalogue, Product Details and database design. Day 2 documents catalogue development, product data and database connection.</sub></p>

<p align="left">
  <a href="../assets/product-backlog/product_catalogue_day_3.png"><img src="../assets/product-backlog/product_catalogue_day_3.png" alt="Product Catalogue Day 3 search filtering availability and discounts checklist" width="46%"></a>
  <a href="../assets/product-backlog/product_catalogue_day_4.png"><img src="../assets/product-backlog/product_catalogue_day_4.png" alt="Product Catalogue Day 4 testing bug fixing and review checklist" width="46%"></a>
</p>

<p align="left"><sub><strong>Figures 3–4.</strong> Day 3 documents search, filtering, availability and student discounts. Day 4 documents browsing tests, search and filter tests, bug fixing and review. Select any image to view it at full size.</sub></p>

**Evidence shown:** The four records connect the Product Catalogue user story to design, data, search, pricing, testing and review activities.

## 3. Trello Evidence

The following links open the specific Product Catalogue cards and consolidated backlog record:

- [Design and database tasks](https://trello.com/c/CbJwEqPR/190-product-catalogue)
- [Development and integration tasks](https://trello.com/c/SUCMkBHx/189-product-catalogue)
- [Search, filtering and pricing tasks](https://trello.com/c/9RbyDtWp/188-product-catalogue)
- [Testing and review tasks](https://trello.com/c/iidvc3Wi/187-product-catalogue)
- [Consolidated Product Catalogue backlog checklist](https://trello.com/c/U1xUQd76/186-product-catalogue)
- [View the complete D6 Food Bulk Product Backlog](https://trello.com/invite/b/69f78ec09a27fa85efb7a81d/ATTI6dfcd3ac97b1d0ff578fd4b64024e3f2A65F99B8/d6-food-bulk)

## 4. Technical Implementation Evidence

### 4.1 TiDB Overview

[TiDB](https://docs.pingcap.com/tidbcloud/tidb-cloud-intro/) is an open-source distributed SQL database. TiDB Cloud provides it as a managed database service that handles infrastructure, scaling and availability while applications use standard SQL.

TiDB is [compatible with the MySQL protocol](https://docs.pingcap.com/tidbcloud/mysql-compatibility/), allowing the application to connect through common MySQL drivers and familiar SQL syntax.

### 4.2 D6 Food Bulk Product Data

D6 Food Bulk uses TiDB as the central data source for the Product Catalogue:

- Product records are stored in the `dfb.products` table.
- Each record contains fields such as `id`, `category`, `contents`, `description`, `food_info` and `image`.
- The application retrieves these records for the website instead of storing catalogue content directly in the page.
- Categories and product data support catalogue organisation and filtering.
- Image paths connect database records to the corresponding product images shown by the interface.

This structure keeps Product Catalogue information in one place and allows product records to be updated without rewriting the interface.

### 4.3 TiDB Product Records

The screenshot shows the query `SELECT * FROM dfb.products LIMIT 100;` and the available Product Catalogue records in the `dfb.products` table.

<p align="left">
  <a href="../assets/product-backlog/tidb_products.png"><img src="../assets/product-backlog/tidb_products.png" alt="TiDB query results showing D6 Food Bulk Product Catalogue records" width="720"></a>
</p>

<p align="left"><sub><strong>Figure 5.</strong> Product records shown in the <code>dfb.products</code> table. Select the image to view it at full size.</sub></p>

**Evidence shown:** The query result documents the Product Catalogue table structure and the product records available from TiDB.

### 4.4 TiDB-Powered Frontend Catalogue

The following interface screenshots show catalogue price filters for students browsing within selected budgets.

#### 4.4.1 Products Under R100

<p align="left">
  <a href="../assets/product-backlog/frontend_under_100.png"><img src="../assets/product-backlog/frontend_under_100.png" alt="D6 Food Bulk catalogue filtered to products under R100" width="320"></a>
</p>

<p align="left"><sub><strong>Figure 6.</strong> Product Catalogue interface displaying products priced below R100. Select the image to view it at full size.</sub></p>

#### 4.4.2 Products Under R200

<p align="left">
  <a href="../assets/product-backlog/frontend_under_200.png"><img src="../assets/product-backlog/frontend_under_200.png" alt="D6 Food Bulk catalogue filtered to products under R200" width="320"></a>
</p>

<p align="left"><sub><strong>Figure 7.</strong> Product Catalogue interface displaying products priced below R200. Select the image to view it at full size.</sub></p>

**Evidence shown:** The two interfaces document Product Catalogue views using the R100 and R200 price filters.
