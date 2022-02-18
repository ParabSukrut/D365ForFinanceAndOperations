This code project has a code which will guide you, if you want to integrate purchase cost from any other system in to D365 for finance and operations. This service creates trade agreement journal header and lines both. All lines are created by reading values coming from JSON payload. If the trade agreement already exist, service sets a to date on it to make it expire. 
You can follow below steps to get this service working.
1.	Download code from Github repo.
2.	Unzip the file and import project or put xml files into your model folder
3.	Refresh models from visual studio and build your model.
4.	Once your build is successful, you can access this service using following endoint

https://YourD365URL/api/services/ASPItemCostImportServiceGroup/ASPItemCostImport/importcost

You can use postman to test this service.
The JSON payload and sample postman request for this service is also part of folder where code is present.
