# Why is there a Contract Mapping website?
Government supports transparency around the services it funds. The Contract Mapping website (http://www.contractmapping.govt.nz/) makes it easy to access funding and contracting information for social service providers. By being open and transparent we improve government accountability for where it spends taxpayer dollars.

# Which government agencies have data on the website?
You will find social service funding and contracting information from:

•	Ministry of Education
•	Ministry of Health
•	Ministry of Justice
•	Ministry of Social Development
•	Te Puni Kōkiri

# Where does the data come from?
Each government agency has provided information on their contracts with social service providers. 
Because the data comes from agencies with different systems and ways of contracting, there will be some variation in the way each agency presents the detail of their contracts. This could include the way the country is divided for contract purposes, how contract volumes are measured, and how the funding is paid to the provider.
Each agency has more specific information relating to their data on the ‘about the data’ pages.

# What information will be shown on the website? 
The website provides information about government funded and contracted social services.
The mapping tool shows you the:

•	name of the provider
•	their address
•	the area in which they deliver their services
•	the type of service delivered
•	the number of clients or services they are contracted to provide
•	how much funding they receive for their services.

Information that may compromise the safety of the people who use the service is not shown e.g. Woman’s Refuge

# How to use these data
Download a zipped dump of a PostgreSQL database (depends on postgis) [here](https://s3-ap-southeast-2.amazonaws.com/govhacknz/data/ministry-of-social-development-msd/contractmapping_data.zip)

Instructions to use this version of the file:
- Download the file above, extract it to an easily accessible location (4GB when extracted)
- Install [PostgreSQL](http://www.postgresql.org/download/) and then [postgis](http://postgis.net/install)
- Open pgAdmin III (installed with PostgreSQL), double-click the default PostgreSQL server, right-click Databases, select "New Database"
- Name the database contractmapping and make its owner postgres
- Select the contractmapping database, then open the PSQL terminal from the Plugins menu at the top
- Type CREATE EXTENSION postgis; to load the postgis extension for this database
- Type \i C:/path/to/file/contractmapping_data.sql to import the downloaded file in to your database
- Back in pgAdmin, navigate to contractmapping>Schemas>public, right-click to refresh, and notice the 16 tables created

Download a zipped set of CSVs representing the tables in the database above [here](https://s3-ap-southeast-2.amazonaws.com/govhacknz/data/ministry-of-social-development-msd/contractmapping_data_csv.zip)