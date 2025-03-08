PubMed Research Paper Fetcher - Project Documentation

1. Project Overview

1.1 Introduction

The PubMed Research Paper Fetcher is a Python-based command-line tool that fetches research papers from PubMed based on a user-provided search query. It extracts essential details and saves the results in a CSV file for easy analysis.

1.2 Purpose

This tool is designed for researchers, students, and professionals who need quick access to relevant research papers. It simplifies the process of retrieving academic papers and filtering out non-academic authors.

1.3 Key Features

Fetches research papers from PubMed API

Supports command-line arguments for flexible usage

Extracts key details: PubMed ID, Title, Authors, Company Affiliations

Saves results in a CSV file for analysis

Implements error handling for API failures

2. Installation & Setup

2.1 Prerequisites

Before running this project, ensure you have the following installed:

Python 3.8+ → Download Python

Poetry (for dependency management, optional)

2.2 Install Dependencies

To install the required Python libraries, run:

pip install requests

If using Poetry, run:

poetry add requests

3. How to Use the Script

3.1 Running the Script

Use the following command to fetch research papers:

python fetch_pubmed.py "cancer research" -f results.csv

Replace "cancer research" with your own query.

The -f flag saves results to results.csv.

Example: Fetching diabetes-related research papers

python fetch_pubmed.py "diabetes treatment" -f diabetes_results.csv

4. Project Structure

backend-project/
│── backend_project/          # Main project folder
│   │── fetch_pubmed.py       # Main script to fetch PubMed papers
│   │── cli.py                # Command-line interface for input handling
│   │── utils.py              # Helper functions (e.g., API requests)
│   │── __init__.py           # Marks this folder as a Python package
│── results.csv               # Output CSV file with research papers
│── diabetes_results.csv      # Another example output file
│── README.md                 # Project documentation
│── .gitignore                # Ignore unnecessary files like __pycache__

5. Code Flow Documentation

5.1 Code Flow Breakdown

User Inputs Query → The program takes a search query as input.

PubMed API Call → The script fetches paper IDs using the PubMed API.

Fetch Paper Details → Extracts details like Title, Authors, Affiliations.

Filter Non-Academic Authors → Detects company-affiliated authors (Currently TBD).

Save to CSV → The results are saved in a structured format.

5.2 Code Flow Diagram

graph TD;
    A[User Inputs Query] --> B[Fetch PubMed Paper IDs]
    B --> C[Fetch Paper Details]
    C --> D[Filter Non-Academic Authors]
    D --> E[Save Results to CSV]
    E --> F[Display Success Message]

6. Future Improvements

Extract company names & author emails automatically

Improve error handling for API failures

Store results in a database instead of CSV

Build a web dashboard for visualization

7. Additional Information

You are free to use LLM tools or other resources to assist in development. The LLM used for this project is GPT.

Clearly document any external tools used in the README.md file.

Assume the program will be evaluated by automated scripts, so strict adherence to conventions is required.

How to identify non-academic authors? You can apply various heuristics such as:

Checking email addresses

Searching for words like "university", "lab", or "institute" in affiliations

Detecting company-associated terms in author details

8. Conclusion

The PubMed Research Paper Fetcher simplifies access to research papers by automating the process of fetching, filtering, and saving key information. Future improvements can enhance its usability and functionality, making it an even more powerful tool for researchers.



