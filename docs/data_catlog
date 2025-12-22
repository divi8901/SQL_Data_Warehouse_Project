**Data Catalog** : gold.dim_customer

  | Column Name          | Data Type | Description                                                                     |
| -------------------- | --------- | ------------------------------------------------------------------------------- |
| `customer_key`       | INT       | Surrogate key uniquely identifying each customer record in the dimension table. |
| `cst_id`             | INT       | Original customer ID sourced from the CRM system.                               |
| `cst_key`            | VARCHAR   | Business customer key used across source systems (e.g., `AW00011000`).          |
| `cst_firstname`      | VARCHAR   | Customer’s first name after trimming and standardization.                       |
| `cst_lastname`       | VARCHAR   | Customer’s last name after trimming and standardization.                        |
| `cst_matrial_status` | CHAR      | Customer marital status (`M` = Married, `S` = Single).                          |
| `gen`                | VARCHAR   | Customer gender in standardized form (`Male`, `Female`, `N/A`).                 |
| `bdate`              | DATE      | Customer date of birth.                                                         |
| `cntry`              | VARCHAR   | Country of residence of the customer.                                           |


  



**Data Catalog** – gold.dim_products

| Column Name         | Data Type     | Description                                                                       |
| ------------------- | ------------- | --------------------------------------------------------------------------------- |
| `product_key`       | INT           | Surrogate primary key for the product dimension, used for joins in fact tables.   |
| `product_id`        | INT           | Business identifier of the product from the source system.                        |
| `category_id`       | VARCHAR       | Code representing the high-level product category from the source system.         |
| `product_number`    | VARCHAR       | Unique product number or SKU assigned to each product.                            |
| `product_name`      | VARCHAR       | Descriptive name of the product.                                                  |
| `cat`               | VARCHAR       | Broad product category (e.g., Bikes, Components).                                 |
| `subcat`            | VARCHAR       | Sub-category within the main product category (e.g., Road Bikes, Mountain Bikes). |
| `product_cost`      | DECIMAL / INT | Standard cost of the product; may be NULL for some component items.               |
| `product_line`      | VARCHAR       | Product line classification (e.g., Road, Mountain).                               |
| `maintenance`       | VARCHAR       | Indicates whether the product requires maintenance (`Yes` / `No`).                |
| `product_strt_date` | DATE          | Date when the product became active or available for sale.                        |
| `product_end_date`  | DATE          | Date when the product was discontinued; NULL if still active.                     |
  

  **Data Catalog**: gold.fact_sales

  | Column Name     | Data Type     | Description                                                                              |
| --------------- | ------------- | ---------------------------------------------------------------------------------------- |
| `order_num`     | VARCHAR       | Unique sales order number identifying a customer purchase transaction (e.g., `SO43697`). |
| `product_key`   | INT           | Surrogate key referencing the product dimension (`gold.dim_product`).                    |
| `customer_key`  | INT           | Surrogate key referencing the customer dimension (`gold.dim_customer`).                  |
| `order_date`    | DATE          | Date on which the sales order was placed.                                                |
| `shipping_date` | DATE          | Date on which the order was shipped to the customer.                                     |
| `due_date`      | DATE          | Expected delivery or payment due date for the order.                                     |
| `sales`         | DECIMAL(12,2) | Total sales amount for the line item (typically `price × quantity`).                     |
| `quantity`      | INT           | Number of product units sold in the order line.                                          |
| `price`         | DECIMAL(12,2) | Unit price of the product at the time of sale.                                           |

