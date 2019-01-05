# Web-Scraping
A technique employed to extract large amounts of data from websites whereby the data is extracted and saved to a local file in the computer or to a database in table (spreadsheet) format

Web scraping of http://www.fallingrain.com/world/IN/ is done in this code.

All error scenarios (e.g. if the website is down or you don’t get the expected response) has been handled properly.

APPROACH :
--------

Request and BeatuifulSoup Library has been mainly used for implementing the code.
The Requests library allows us to make use of HTTP within our Python programs in a human readable way, and the Beautiful Soup module is designed to get web scraping done quickly.

Links/URL at different level changes by just single character.
For Example : 
Cities in Rajasthan, starting with 'J' has link : http://www.fallingrain.com/world/IN/24/a/J/
and starting with 'Ja' has link : http://www.fallingrain.com/world/IN/24/a/J/a/
Thus we add characters to the link, to get onto next-level.


Firstly, we generate links and then check whether the given link or url is active or not.

If the url is active, then we see whether the given webpage contains the required data in the form of 'City', 'Latitude', etc. or the links leading to next level. 

If webpage contains required data, then the data is added to the Pandas Dataframe, so that data manipulations can been done easily.

If it contain only links to the next-level, then we generate next-level url and repeat the procedure.

Required data is tagged under 'td' tag, which is tagged under 'tr' tag, thus if soup object has 'tr' tag, then we need to add the data to our dataframe.

If we only have 'href' tag, then we need to go onto next-level to fetch required data.

Lastly pandas dataframe is exported to CSV file.


REFERENCES : https://www.digitalocean.com/community/tutorials/how-to-scrape-web-pages-with-beautiful-soup-and-python-3
