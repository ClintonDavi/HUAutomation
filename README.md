### Top_Up_From Warehouse.ipynb ###
This script distributes stocks to retail shops based on demand and sales. Another file called min max is fed into the model. This file has the minimum and maximum inventory levels of all items for all the 32 retail shops. 
Other model inputs include instock status and gross profit margin

**Logic**
 - Create two tables, move from and move to tables.
 - Move from tables is simply positive inventory of warehouse items. Move to tables is positive inventory of products in the shops.
 - If an item is understocked in the shops, model will recommend that X units of the item to be moved to the shop from the warehouse.
 - Distribution occurs in a structured order - shop with zero instock is supplied first followed by shop with the highest deficit i.e shop that has the capacity to hold the most (calculated as maximum inventory - instock). A for loop distributes the products untill all shops are filled to their maximum levels.
   
**Output**
- An excel file that clearly shows what units to move and where to move them.
