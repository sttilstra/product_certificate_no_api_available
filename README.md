This script was created for use as an azure function to ultimatley populate a sql table with a url/web link to a product certificate. This information is part of a larger project and puts these values into a sql table which feeds a web application. As part of this application, users are able to click the link and download the certificate directly.

Outside of navigating to the site, searching for a product code and navigating several screens, the website which houses the certificates does not really have a way of getting the certifacte links - at least easily. No Api is avaialble. 
This required a two stage http request approach in order to get to the actual link which allows users to download the product certificate. Class objects are created based on the respones.
Thie script joins two sql tables and looks for rows where we do not have a certificate link available. It then makes a couple different http requests and ultimately add new records to the database and checks for updates for existing records.
