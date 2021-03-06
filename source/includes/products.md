#Products

##Index

List of products

`GET /api/products`

**Parameters**

Parameter | Function | Form
--------- | -------- | ----
page | To get an specific page of products | `GET /api/products?page=2`
per_parge | The number of products to get per page | `GET /api/products?per_page=25`

**Successful status**

`Status code: 200`

> Request response

```
{
	"pages": 5,
	"currentPage": 1,
	"count": 25,
	"products": [
		{
			"productId": 1,
			"name": "Example product",
			"description": "This is the description for a product",
			"displayPrice": "15.99",
			"permalink": "ruby-on-rails-tote",
			"availableOn": "2012-10-17T03:43:57Z",
			"images": {
				"miniUrl": "https://bucket.com/12343242323423",
				"smallUrl": "https://bucket.com/12343242323423",
				"normalUrl": "https://bucket.com/12343242323423",
				"largeUrl": "https://bucket.com/12343242323423"
       		}
       }
   ]
}
```

##Show

Details of a product

By _permalink_:

`GET /api/products/a-product`

By _id_:

`GET /api/products/123`

**Successful status**

`Status code: 200`

>Request response

```
{
	"master": {
		"productId": 1,
		"name": "Example product",
		"description": "This is a product example.",
		"displayPrice": "15.99",
		"permalink": "ruby-on-rails-tote",
		"inStock": true,
		"availableOn": "2012/10/17 14:04",
		"images": {
				"miniUrl": "https://bucket.com/12343242323423",
				"smallUrl": "https://bucket.com/12343242323423",
				"normalUrl": "https://bucket.com/12343242323423",
				"largeUrl": "https://bucket.com/12343242323423"
       }
	},
	"variants": [ 
		{
			"productId": 1,
			"name": "Example product",
			"description": "This is a product example.",
			"displayPrice": "15.99",
			"permalink": "ruby-on-rails-tote",
			"inStock": true,
			"availableOn": "2012/10/17 14:04",
			"images": {
					"miniUrl": "https://bucket.com/12343242323423",
					"smallUrl": "https://bucket.com/12343242323423",
					"normalUrl": "https://bucket.com/12343242323423",
					"largeUrl": "https://bucket.com/12343242323423"
       	}			
		},
		{
			"productId": 1,
			"name": "Example product",
			"description": "This is a product example.",
			"displayPrice": "15.99",
			"permalink": "ruby-on-rails-tote",
			"inStock": true,
			"availableOn": "2012/10/17 14:04",
			"images": {
					"miniUrl": "https://bucket.com/12343242323423",
					"smallUrl": "https://bucket.com/12343242323423",
					"normalUrl": "https://bucket.com/12343242323423",
					"largeUrl": "https://bucket.com/12343242323423"
       	}			
		}
	]
}
```