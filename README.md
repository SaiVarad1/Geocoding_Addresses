# Geocoding_and_Reverse_Geocoding_Addresses

* Code generates geographical coordinates and then use reverse geocoding to generate addresses for address-input verification as well as Google URLs based on a CSV file containing info on customer addresses.
* Output is a CSV file with the new columns, Latitude, Longitude, Generated Address, and Google URL
* Uses Python,Google Maps API, parallel processing and batch calls to improve performance for large input files 
* NOTE: You need an API Key to use the Google Maps API, found here: 
  
Example Usecase:
Input CSV File containing the data:

Customer_Name | Address_1| Address_2| City   | Zip    | State
Cust_A        |123 Apt A | Street A | A_city | 123456 | AZ
Cust_B        |456 Apt B | Street B | B_city | 1242342| CA

Output File:

Customer_Name | Address_1| Address_2| City   | Zip    | State | Concatenated Address           | Latitude | Longitude | Generated_Address | Google_URL
Cust_A        |123 Apt A | Street A | A_city | 123456 | AZ    |123 Apt A,Street A,A_city,123456| 
Cust_B        |456 Apt B | Street B | B_city | 1242342| CA
