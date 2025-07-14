# Job Scraping

## Overview
The notebook is structured into several sections:

* Imports and Constants: Imports necessary libraries and defines constants like user agents for rotation and target African locations.
* Rate Limiting & User Agent Rotation: Includes helper functions to introduce random delays and rotate user agents for ethical scraping and avoiding rate limiting.
* URL Construction & Page Fetching: Functions to construct search URLs for LinkedIn and fetch the HTML content of job listing pages.
* Extract Job IDs from Listing Page: Extracts individual job IDs from the LinkedIn search results page.
* Fetch and Parse Individual Job Postings: Fetches detailed information for individual job postings from LinkedIn.
* Utility Function for Safe Text Extraction: A helper function to safely extract text from HTML elements.
* Full Scraping Routine per Location: The main function to scrape LinkedIn jobs for a given title and location across multiple pages.
* Main Execution and Data Processing: Runs the LinkedIn scraper for all defined African locations, enriches the data with skill indicators, and saves the results to a CSV file.
