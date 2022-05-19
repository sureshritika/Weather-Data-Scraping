# Weather-Data-Scraping

**Objective:** Build a website to track the extended weather forecast for five designated cities
in the state of New Jersey from https://forecast.weather.gov.

**Task:** The center piece of the website is a dashboard that shows the day and night extended
weather forecast for a preferred city, out of five designated cities, in the state of New Jersey.
The information related to each city include:
```
City Name , Date , Day or Night , Temperature , Short Description , Long Description
```

Refresh the content of the website every six hours. The dashboard should allow the selection
of any city out of the five designated cities.

Lastly, the website must support homepage personalization. This includes the ability to
choose a preferred city out of the five designated ones. The information should be stored in
the database paired with the visitor’s IP address.

**Deliverables:** The `.zip` file must contain the following
files:

1. **A text file named _`sources.txt`_**. The file must contain the exact five source URLs
used for retrieving all website data.

2. **A shell script named _`weather.sh`_**. The script should automatically repeat the
following steps every six hours:
    - Download the weather Web page for the designated number of cities.
    - Call TagSoup to generate a `.xhtml` file that corresponds to each downloaded `.html` file.
    - Execute **a Python script named _`parser.py`_** that uses the `xml.dom.minidom` module to traverse the `.xhtml` documents one file at a time, extract the relevant data, and insert the extracted data into a MySQL database.

3. **PHP scripts** that make the website, and static **`.html` files** , along with embedded
**images** , if any.
    - Execute **a PHP script named _`njweather.php`_** that runs the initial dashboard page with links to the other cities.

4. **A dump of the database definitions and table data**. A MySQL dump exports the data stored in the MySQL database into a `.sql` file.
