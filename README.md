# Scraping a Job Advert to Map Keyword Frequency

## Overview

This Python project scrapes text from an online job advertisement and analyzes the frequency of keywords within the ad. The primary goal is to help job seekers tailor their resumes and applications by highlighting the most emphasized skills and qualifications. The project demonstrates the use of Python for web scraping, text processing, and data analysis, utilizing the BeautifulSoup, requests, and pandas libraries.

Note: The original script was used to scrape a job advert from the Norwegian site finn.no, however, to show respect for finn.no's policies, I used Chat GPT to create a fake & very similar HTML code for demonstration purposes in the Jupyter Notebook preview.

## Features

- **HTTP Status Check**: Verifies the accessibility of the webpage before scraping.
- **Web Scraping**: Extracts and parses the HTML content of a job ad using BeautifulSoup.
- **Text Processing**: Cleans and splits the job ad text into individual words.
- **Keyword Frequency Analysis**: Counts the frequency of each word and stores the results in a CSV file.

## How It Works

1. **CheckSoupStatus Function**:  
   The function `CheckSoupStatus(url)` checks the HTTP status code of the provided URL and prints a message indicating whether the request was successful (200 OK) or if there was an error (e.g., 404 Not Found).

2. **Web Scraping**:  
   The script sends a GET request to the job ad URL, parses the HTML content with BeautifulSoup, and extracts the title and the main job ad text.

3. **Text Processing**:  
   The job ad text is processed by splitting it into individual words using a regex pattern that handles various separators, including spaces and punctuation. The words are then converted to lowercase and cleaned of empty entries.

4. **Keyword Frequency Analysis**:  
   The frequency of each word is counted and analyzed using Pandas, and the frequency of each word is stored in a DataFrame. The resulting data is saved to a CSV file (`word_list.csv`) for further analysis.

## Technologies Used

- **Python**: For scripting and data processing.
- **BeautifulSoup**: To parse and navigate the HTML content.
- **Requests**: To handle HTTP requests and fetch web content.
- **Pandas**: For data manipulation and analysis.
- **Regex**: To split and clean the text data.

## Future Improvements
- Remove widely used words (such as "and", "the", "a") from the output to provide more meaningful information - can use the Natural Language Toolkit (NLTK) library for this.
- Compare (%-based) the output to a CV/resume, so the user can see how well their skillset matches the job.
- Group the output into categories (such as hard skills, soft skills, technologies, platforms, techniques), to get a clear overview of the skills the company is looking for.
