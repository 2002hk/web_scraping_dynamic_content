## Web scraping Dynamic Content from https://directory.ntschools.net/#/schools
## Libraries used
- scrapy
- ipython
- virtualenv
## Project Structure
```bash
univscraper/
│── venv/
│── univscraper/               # Project module
│   ├── spiders/                # Spider definitions
│   │   ├── __init__.py
│   │   ├── univspider.py        # Custom spider
│   ├── __init__.py
│   ├── items.py                # Define scraped data structure
│   ├── middlewares.py          # Custom middlewares
│   ├── pipelines.py            # Data processing pipelines
│   ├── settings.py             # Scrapy settings
│── scrapy.cfg                  # Scrapy configuration file
│── requirements.txt            # Dependencies
│── README.md                   # Project documentation
```
## Commands used
```bash
## to create virtual env
python -m venv venv
python venv\Scripts\activate
## to create project
scrapy startproject univscraper
## go the spider folder
scrapy genspider univspider '##paste webpage url'
## to activate scrapy shell
scrapy shell
```
- Uses Scrapy to make API requests instead of parsing HTML.
- Extracts structured JSON data directly from the server.
- Avoids getting blocked by using custom headers.
- Uses multiple callbacks to handle different request responses.
- This is a clean and efficient approach for web scraping using APIs!
