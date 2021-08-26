# DEAR Inventory Integrations with Zapier
A collection of notes /code snippets for setting up DEAR Inventory API on Zapier

Zapier App is currently private/email only and set up for a client - if interested please contact and I will forward to you

# POST /CUSTOMERS

1. List Contacts and Addresses as Parent Keys. Be sure to check "include in JSON body"

2. Using the Create endpoint for the POST API request requires a workaround as there is a "Name" field for both Customers and Contacts

Example structure

```javascript
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
```
# namescript 

Node 4.3.2

To handle Zapier issue in not being able to have the "Name" key for both Customer and Contact sub-dictionary 

# addresscontacts

Node 4.3.2
To handle a flat structure (this example was a hubspot form) with multiple contacts, addresses, to map to the sub-dictionary 
