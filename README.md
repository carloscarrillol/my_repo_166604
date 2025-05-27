# my_repo_166604
This repository contains the final project for Econometrics II, which builds a reproducible and well-documented data scraping pipeline using the YouTube Data API v3. The goal is to collect at least 500 comments from recent videos of a specific YouTube channel and store them in a structured dataset.

Project Structure

The repository is organized as follows:


your-repo/
├── README.md (this file)
├── .gitignore (ignores secret and unnecessary files)
├── requirements.txt (pinned dependencies for reproducibility)
├── code/
│ └── scrape_comments.py (main scraping script)
└── data/
  └── dataset.csv (final dataset with scraped comments)

Setup Instructions

Clone the repository by running:

git clone https://github.com/your-username/your-repo.git

cd your-repo

Create a .env file in the root directory and add your YouTube Data API key:

API_KEY=your_youtube_data_api_key_here

Install the required Python libraries using pip:

pip install -r requirements.txt

How to Run the Scraper


To run the script and scrape comments, execute:
python code/scrape_comments.py

This will collect comments from the 10 most recent videos of the YouTube channel "Sliinky" (or whichever channel is defined in the script) and save them to a file named dataset.csv in the data folder. Each row of the dataset includes the comment ID, comment text, and the ID of the video where the comment was posted.

Dataset Structure

The resulting dataset will be a CSV file with the following columns:

comment_id: unique identifier of each comment
text: plain text of the comment
video_id: identifier of the corresponding video
Example:

comment_id, text, video_id
UgzrBQJMb9wxyz, "Nice video!", a1b2C3d4E5F
Ugy7WpLsPzqvABC, "Awesome content!", a1b2C3d4E5F

Reproducibility

All packages are listed in the requirements.txt file with pinned versions to ensure reproducibility. The list includes only the libraries explicitly used in the script. To reproduce the environment, it is recommended to use a virtual environment and run:
pip install -r requirements.txt

Notes

If a video has comments disabled or contains fewer than 100 comments, the script will retrieve only the available data.
The script can be modified to search for a different channel by changing the query string in the search request.
A short delay may be added between requests to avoid exceeding API rate limits.
References

YouTube Data API v3 documentation
Google API Python Client
python-dotenv documentation
Author

Carlos Carrillo
Final Project for Econometrics II
May 2025


