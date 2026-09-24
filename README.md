## Overview

The Store Management Platform supports day-to-day retail operations across multiple applications, including administration, sales, consignment, reporting, product management, and customer-facing storefront functionality.

The platform is designed as an integrated system consisting of:

- Web-based administration portal
- Mobile administration application
- Backend REST API
- Customer storefront

## Key Features

- Product and category management
- Sales management
- Consignment management
- Distributor management
- Expense tracking
- Reporting
- Accounts receivable
- Role-based access control
- Mobile administration
- Customer storefront
- Social media publishing integration

## Technology Stack

- C#
- .NET
- ASP.NET Core
- Entity Framework Core
- SQL Server
- Blazor
- Flutter
- Next.js
- JWT Authentication
- IIS
- CI/CD

## Database Design

The system uses a relational SQL Server database supporting products, sales,
inventory, customers, distributors, consignments, receivables, and payments.

### Entity Relationship Diagram

<img width="2846" height="1787" alt="RV Store Entity Relationship Diagram" src="https://github.com/user-attachments/assets/ea0893f5-fc22-43e6-b91b-ea1d2532da35" />

## Process Flows

### Point of Sale

<img width="1270" height="1521" alt="Process Flow" src="https://github.com/user-attachments/assets/460eec84-0354-4772-bc10-df7d532ee8d9" />

### Consignment

<img width="932" height="1061" alt="RV Store Consignment Process Flow" src="https://github.com/user-attachments/assets/fe85e483-f13c-4820-adfe-0ba27c249b18" />

Consignment Settlement

<img width="994" height="960" alt="RV Store Consignment Settlement Process Flow  (1)" src="https://github.com/user-attachments/assets/41c41a9f-f4ce-468f-b787-19fb2d388e8f" />



## CI/CD and Deployment

The Store Management application uses an automated CI/CD workflow to improve deployment consistency and reduce manual errors.

### Pipeline Capabilities

- Builds and validates the .NET solution before deployment.
- Runs automated unit and regression tests as part of the pipeline.
- Builds the Blazor Admin Web application, including Tailwind CSS assets.
- Publishes the Store API and Admin Web applications for IIS hosting.
- Maintains separate UAT and Production deployment environments.
- Uses environment-specific application configuration for API endpoints, database connections, authentication, CORS, and other settings.
- Preserves runtime content such as uploaded product images during deployments.
- Prevents deployment from continuing when build or automated test validation fails.
- Includes post-deployment verification of the deployed application and API endpoints.

### Deployment Architecture

- **Backend:** ASP.NET Core / .NET 10 API hosted in IIS
- **Admin Web:** Blazor Server hosted in IIS
- **Admin Mobile:** Flutter application consuming the same Store API
- **Storefront:** Next.js application consuming the Store API
- **Database:** SQL Server with Entity Framework Core
- **Environments:** Separate UAT and Production configurations

The CI/CD process is designed to provide repeatable deployments while ensuring that application builds, automated tests, environment configuration, and runtime assets are validated before a release reaches Production.

## My Role

I designed and developed major parts of the platform, including:

- Backend API development
- Web administration development
- Mobile application development
- Database integration
- Authentication and role-based authorization
- Business rule implementation
- Reporting features
- Deployment configuration
- UAT and production environment support
- External integration development

## Screenshots

### Products Catalog

The Product Catalog provides a centralized interface for managing store products and their core information. It is designed to make product maintenance fast, organized, and easy to use from a desktop environment.

Key capabilities include managing product names, categories, brands, sizes, pricing, product images, and other product-related details. The catalog also supports searching, filtering, sorting, and reviewing products efficiently, making it easier to maintain an accurate and consistent product inventory.

The module is built with maintainability and scalability in mind, allowing additional product attributes and business rules to be introduced as the system continues to evolve.

<img width="1069" height="823" alt="product-management" src="https://github.com/user-attachments/assets/17cb66d1-2756-4ac6-a0cb-d6a9250cefc1" />


### Point of Sale

The Point of Sale module provides a streamlined interface for processing walk-in sales efficiently. Products can be quickly located using search, brand, category, and item filters, then added directly to the current order without leaving the sales screen.

The interface displays product images, pricing, available stock, and low-stock indicators to help staff make informed decisions during checkout. Selected items are managed in a real-time order panel where quantities can be adjusted, items removed, and transaction remarks recorded.

The module also calculates the running subtotal and total amount due, while allowing transactions to be saved as drafts or continued to the payment process. The layout is optimized for fast cashier workflows, minimizing unnecessary navigation and keeping product selection and order management on a single screen.

<img width="1321" height="823" alt="point-of-sale" src="https://github.com/user-attachments/assets/6002b3ba-da99-40be-bd88-f4cbd2ff4cec" />


### Consignment Management

The Consignment Management module provides a structured workflow for releasing products to distributors while keeping product selection, partner details, and consigned items visible on a single screen.

Users can search and filter products by brand, category, and item type, review available stock and distributor pricing, and add selected products to the consignment release. The transaction panel allows staff to select the active distributor, specify an optional due date, and record remarks or handling instructions.

Selected products appear in a dedicated released-items panel where quantities can be adjusted or removed before the consignment is finalized. The system automatically calculates the total consignment value based on the applicable distributor pricing.

Consignments are initially prepared as drafts, allowing the transaction to be reviewed before confirmation. Inventory remains unaffected during draft preparation and is only updated once the consignment is formally confirmed, helping maintain accurate stock control and a clear transaction workflow.

<img width="1335" height="781" alt="consignment screen" src="https://github.com/user-attachments/assets/95868af2-ba6a-4872-b5d2-698d7af6be95" />


### Reporting

The Reporting module provides operational and financial visibility across the store through structured, export-ready reports.

The Inventory Report summarizes key metrics such as total products, total units on hand, inventory cost valuation, potential selling value, and gross margin. Detailed product-level information includes brand, category, quantity, cost, distributor price, selling price, cost value, and current product status.

Reports can be filtered to focus on relevant data and are displayed directly within the application for review. Users can also download reports as PDF files for sharing, record keeping, or offline analysis.

The reporting interface is designed to give administrators a clear view of inventory performance while keeping the underlying calculations consistent with the Store API and current store data.

<img width="1093" height="733" alt="inventory-reports" src="https://github.com/user-attachments/assets/572f3868-6fa9-4a4f-88bc-c4659db8fb0c" />


### Role Access

The Role Access module provides centralized control over what each user role can view and manage within the Store Administration system.

Administrators can select a role and configure permissions across major functional areas such as Products, Catalog, Customers, Consignments, Cash Remittance, Dashboard, and other administrative modules. Permissions are defined at the action level, allowing access to be controlled separately for capabilities such as viewing, creating, editing, managing, confirming, or cancelling records.

The interface groups permissions by module to keep access rules easy to review and maintain. Changes can be applied to the selected role without modifying the underlying application workflow.

This role-based permission model helps enforce least-privilege access, keeps responsibilities clearly separated between administrators, managers, and staff, and makes the system easier to maintain as new modules and actions are introduced.

<img width="898" height="825" alt="role-access" src="https://github.com/user-attachments/assets/614c3efb-e007-4545-8e67-20911f53aca8" />


## Project Type

Freelance / Portfolio Project

## Source Code

The source code for this project is private. This repository is intended as a portfolio showcase of the application's functionality and user interface.
