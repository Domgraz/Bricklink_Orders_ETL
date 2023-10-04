# Bricklink_Orders

## Table of Contents:
* [Background](#background)
* [Techologies and Libraries](#technologies-and-libraries)
* [ETL Process](#etl-process)
* [Data](#data)


## Background
Bricklink is a selling platform for Lego, where indivdual parts, minifigures, sets, etc can be bought and sold across the world. 
I opened a online store within Bricklink in August of 2023 and have wanted to store data related to my sold orders. I wanted something 
more than concatenating the csv file for each month and decided to create a database in MySQL to house this data.

## Technologies and Libraries

* Python 3.9
* Pandas
* MySQL and it's Python connector
* glob
* os
* csv


## ETL Process
* Extract - data was downloaded manually as csv files through my Bricklink login, to get the data on orders through my store
* Transform - using Python in the jupyter notebook, within a pandas dataframe the data was cleaned, columns reformatted, date and time were changed, and columns were stripped of $
* Load - using Python in the jupyter notebook, using the mysql connector, a database was created and then populated with the output csv from the transform phase



## Data 
* Order ID - overall ID of the order
* Order Date - date that the order was made
* Buyer - user name of the buyer
* Base Currency - currency paid in
* Shipping - price of shipping
* Order Total - price of the order
* Tax - tax calculated on the order
* Base Grand Total - total price of the order including, order total, shipping, and tax
* Total Lots - number of different type of items in the order
* Total Items - total items in the order
* Order Status - status of the order (packed, shipped, completed, etc.)
* Location - location of the buyer, usually the state they reside in
* Condition - condition of the item (used or new)
* Item Description - description of the item as provided on Bricklink
* Qty - number of same pieces in order
* Each - individual price of each piece
* Total - total price of same pieces in order
* Item type - category of item (part, minifigure, etc.)
* Item Number - item number as provided by Bricklink and Lego
* Inv ID - id specific to the part within the order
  
