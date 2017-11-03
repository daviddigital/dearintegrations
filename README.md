# dearintegrations
A collection of notes /code snippets for setting up DEAR Inventory API on Zapier

Zapier App is currently private/email only and set up for a client - if interested please contact and I will forward to you

# POST /CUSTOMERS

1. List Contacts and Addresses as Parent Keys. Be sure to check "include in JSON body"

2. Using the Create endpoint for the POST API request requires a workaround as there is a "Name" field for both Customers and Contacts

Example structure

{
 "Addresses": [
 {
 "Line1": "The First ave",
 "Line2": "",
 "City": "City X",
 "State": "NewState",
 "Postcode": "12345",
 "Country": "US",
 "Type": "Shipping",
 "DefaultForType": true
 },
 {
 "Line1": "The First ave",
      "Line2": "",
 "City": "City X",
 "State": "NewState",
 "Postcode": "12345",
 "Country": "US",
 "Type": "Billing",
 "DefaultForType": true
 }
 ],
 "Contacts": [
 {
 "Name": "John Smith",
 "Phone": "1-555-555-55-55",
 "Email": "email@sample.com",
 "Default": true
 }
 ],
 "Name": "Sample Company",
 "Currency": "USD",
 "PaymentTerm": "30 days term",
 "Discount": 0,
 "TaxRule": "Tax on Sales",
 "Carrier": "DHL",
 "Location": "Main Warehouse",
 "Comments": "Sample customer",
 "AccountReceivable": "610",
 "RevenueAccount": "200",
 "PriceTier": "Default Price Tier",
 "Tags": "sample, customer",
 "Status": "Active",
 "CreditLimit": 0
}

Zapier Fields: 

Label	Key	Dynamic Dropdown	Required	Sort	Actions
Discount	Discount	none		 	 Edit   Delete
AdditionalAttribute1	AdditionalAttribute1	none		 	 Edit   Delete
Contact's Name	Name	none		 	 Edit   Delete
Contact's Default	Default	none		 	 Edit   Delete
Contact's Phone	Phone	none		 	 Edit   Delete
Contact's Fax	Fax	none		 	 Edit   Delete
Contact's Email	Email	none		 	 Edit   Delete
Contact's Website	Website	none		 	 Edit   Delete
Contact's Comment	Comment	none		 	 Edit   Delete
Contact's IncludeInEmail	IncludeInEmail	none		 	 Edit   Delete
Customer Name	Customer_Name	none		 	 Edit   Delete
Currency	Currency	none		 	 Edit   Delete
PaymentTerm	PaymentTerm	none		 	 Edit   Delete
TaxRule	TaxRule	none		 	 Edit   Delete
AccountReceivable	AccountReceivable	none		 	 Edit   Delete
Revenue Account	RevenueAccount	none		 	 Edit   Delete
Status	Status	none		 	 Edit   Delete
Carrier	Carrier	none		 	 Edit   Delete
Sales Representative	SalesRepresentative	none		 	 Edit   Delete
Location	Location	none		 	 Edit   Delete
Comments	Comments	none		 	 Edit   Delete
Price Tier	PriceTier	none		 	 Edit   Delete
Tax Number	TaxNumber	none		 	 Edit   Delete
Tags	Tags	none		 	 Edit   Delete
Credit Limit	CreditLimit	none		 	 Edit   Delete
Address Default for Type	DefaultForType	none		 	 Edit   Delete
Address Line1	Line1	none		 	 Edit   Delete
Address Line2	Line2	none		 	 Edit   Delete
Address City	City	none		 	 Edit   Delete
Address State	State	none		 	 Edit   Delete
Address Postcode	Postcode	none		 	 Edit   Delete
Address Type	Type	none		 	 Edit   Delete
Address Country	Country	none		 	 Edit   Delete
