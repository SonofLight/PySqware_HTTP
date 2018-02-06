# PySqware
A simple module for the Django Framework to use with the Square API. 

Rather than having to upload products into two seperate systems, users can use this program to 
update web applications in real time as changes are madeto square accounts (IE: products, categories, etc.).

Any changes made to the Square Dashboard or POS system will reflect on the web application in real time. 

Square Business/Merchant Account needed before using.


## Version 0.3.0

written using Python 3


## Features

#### Recently Added Feature(s):
+ Added Customer module - CRUD module with sq_customer class for customers (create customer, check email, update customer, update email, delete account.)

#### Previously Added Feature(s):
+ Added catalog module - catalog module collects and creates json data of categories and items from API. It also has a product module that allows items associated with a category_id to be returned for data manipulation.
+ Added Sq_Connect class with a connect_api function for connection to Square api.



## Connect - Sq_Connect Class


#### Read First

If you have not created a square business account, please do so before continuing.
The Connect class assumes that you have already set-up a square merchant account and have access to 
the following square credentials:

+ Access Token
+ Application ID 
+ Location(s) ID

#### Secrets.py and Secrets.json
Before you are able to use the Square API or Sq_Connect class, you have to first create your secrets.json file to use with the secrets.py file.
Rather than hard coding your Access Token, Application ID, and Location ID headers everytime you send a request, these two files ensure that you only have
to set-up once as well as protect your sensitive data.

##### Secrets.py
There are two global variables : **BASE_DIR and  SECURITY KEY**

```
BASE_DIR = os.path.dirname(os.path.abspath(__file__))
SECURITY_KEY = os.path.join(BASE_DIR, 'secrets.json')
```

They are currently set to the **connect** module file path. You can change the file path to your desired path.

Just remember to assign the **SECURITY_KEY** file path to where you will be storing your secrets.json file.

#### Endpoints

The Sq_Connect class utilizes the **GET, POST, PUT, DELETE** http methods through the Requests library. These methods conincide with the 
CRUD endpoints of the Square API: [Endpoint Names and Return Values](https://docs.connect.squareup.com/api/connect/v2#endpointnamesandreturnvalues "Endpoint Names and Return Values"). 




## License:


This project is licensed under the MIT License.