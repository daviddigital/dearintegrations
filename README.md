# dearintegrations
A collection of notes for setting up DEAR Inventory API on Zapier

1. Using the Create endpoint or the POST API request requires a workaround as there is a "Name" field for both Customers and Contacts. 

2. List Contacts and Addresses as Parent Keys

Zapier App is currently private/email only - if interested please contact and I will forward to you

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

