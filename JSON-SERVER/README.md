# JSON SERVER 
NPM package  that lets us create false REST APIs for Prototyping


<h1 align="center"> Some Important Features to know in json server: </h1>


## GET REQ or FETCHING DATA

* Example: http://localhost:3000/products

* Example: http://localhost:3000/reviews


### FILTERING

* Example: http://localhost:3000/products?category=electronics&discount.type=shipping

### SORT

* Example: http://localhost:3000/products?_sort=price

* Descending: http://localhost:3000/products?_sort=price&_order=desc

* by category in ascending and price in descending: http://localhost:3000/products?_sort=price,category&_order=desc,asc

### Pagination

* http://localhost:3000/products?_page=1
* http://localhost:3000/products?_page=1&_limit=2   etc. 

### Operators

* >= & <= : ### http://localhost:3000/products?price_gte=2000&price_lte=6000

* !=: http://localhost:3000/products?id_ne=1

* like operator that lets you specify regex to filter data: http://localhost:3000/products?category_like=^f  --- filter all products starting with 'f'

### Full Text Search (q - query parameter)

* Exanple: http://localhost:3000/products?q=in

### Relationships

* http://localhost:3000/products?_embed=reviews
* http://localhost:3000/products/1?_embed=reviews 

* for fectching parent resources 
* http://localhost:3000/reviews/1?_expand=product

## POST REQUEST

* Implemented using Thunder Client extension on vs code 
* In real time coding its done through Axios

## PUT, PATCH , DELETE
 
* Implemented using Thunder Client extension on vs code 
* In real time coding its done through Axios

## Configurations

* specifying port number- Default is 3000, we specify in the [package.json](./package.json): serve-json script the port to run our server to avoid conflicts with other applications like React that run on port 3000

* Custom routes [routes.json](./routes.json) specified further in [package.json](./package.json) scripts

## Generate Random Data

[data.js](./data.js) 

Other data sources [libraries] are: 
* chancejs
* casual
* fakerjs