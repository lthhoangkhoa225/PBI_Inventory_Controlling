# PBI_Inventory_Controlling
## I. Introduction
### 1. Business question
The production department identified the following requirements and want the Data team to support: Help users review the inventory status of each product category in a quicker and more convenient way 
therefore adjustment to business operation, marketing activities, sales, ...
### 2. Dataset
Dataset: adventureworks2019 (public Google BigQuery dataset)

Dataset dictionary: Please reach file "Data Dictionary" attached above

Dataset Schema: https://i0.wp.com/improveandrepeat.com/wp-content/uploads/2018/12/AdvWorksOLTPSchemaVisio.png?ssl=1

Dataset access:

- Log in to your Google Cloud Platform account and create a new project.
- Navigate to the BigQuery console and select your newly created project.
- In the navigation panel, select "Add Data" and then "Star a project by name".
- Enter the project name "adventurework2019"
## II. Apply design thinking mindset
### 1. Empathize
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/70b6c2b0-14af-4e02-bde7-c2977d8688bc)
### 2. Define point of view
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/38a72302-6981-4a81-b81e-ea3c4c81d8eb)
### 3. Ideate
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/779a6a39-22dc-43f6-a94a-024306bbc871)
### 4&5. Prototype and review
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/75bc75fe-83d3-42dd-9d4e-87bdf88f5078)
## III. Main process
### 1. Connect data to PBI and modelling
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/3014f2cb-e729-42cb-ae86-831b68a0c1d3)
### 2. Build dashboard
- Using DAX to create measures and calculated columns
- Build 3 report pages
### Product Inventory Overview
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/e581413b-71f7-4fc0-8f41-a8c3ef208de2)
### Operate Inventory Products
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/d3046f9b-e702-4080-b5c8-26dcb853a08a)
### Product Inventory Detail
![image](https://github.com/lthhoangkhoa225/PBI_Inventory_Controlling/assets/168264791/ba0e31b0-7695-445b-9826-e279c57483a4)
## IV. Fact & Insights
### Fact
- The overall situation of inventory is quite good. The number of items is at a high safety level, the number of items reaching the reorder point is low.
- However, there are some problems: many items are stored but are not actually sold. This causes the company to have a backlog in production budget as well as storage costs. Many items have quantities that exceed the Safety Stock Level too much, which shows that the production budget is unevenly distributed.
- The number of products in stock varies between warehouses. Having items stored in multiple locations can make it difficult to control inventory.
### Insights
- Total inventory is approximately 336,000 products. Total inventory is 432 items. But the quantity for sales is approximately 326,000 products and 386 items.
Of the 386 items being sold, 318 items meet the Safety Stocked Level. It can be seen that compared to 363 items reaching Safety Stocked Level across all warehouses, there are 45 items at this level or more but are not for sale.
- When comparing the total cost and production quantity of 318 items being sold to reach Safety Stocked Level and the minimum cost and quantity to reach Safety Stocked Level of the above items. We see a pretty big difference of 13.4 million (Dollar) versus 8.2 million (Dollar) in cost and 276 thousand versus 173 thousand in quantity.
- The number of products being sold at or below the reorder point is 7 products, of which 3 products are completely out of stock.
- For products that are not for sale and are still in stock. There are a total of 46 items, approximately 10 thousand products, total production cost is 6.5 million (Dollar). If these products are sold, they can bring in up to 11.2 million (Dollar) in revenue.
## V. Recommendations
- The Production department should stop producing products that meet the Safety Stocked Level and products that are no longer for sale. Prioritize the production of 3 products that are on sale but are out of stock in addition to 4 products at reorder level. Next is the production of products below the safety stocked level.
- Besides, you should allocate storage locations appropriately to avoid the situation where one location has full capacity while another location has a lot of space. Each item should only be stored in a certain location, to facilitate the import and export of each item as well as make it easier to control the storage status.
- For those in stock but no longer for sale. The Sales and Marketing department comes up with strategies such as bundling with other products and selling at a reasonable price to partly free up the cost of producing the above product.
- The Sales and Marketing departments coordinate to market and sell overstocked items. Especially in the Top 10 products with the most inventory, up to 9 products are Hex Nut.
