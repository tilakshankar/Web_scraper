# Web_scraper
1️⃣ Step-by-Step Breakdown:

🔍 1. Search for Relevant Websites
It uses Google Search (googlesearch module) to find the top 10 websites related to fintech, consulting, finance, market trends, and strategy.

The search query "The Digital Fifth fintech OR consulting OR finance OR market trends OR strategy" ensures it finds articles, reports, and insights related to these topics.

🌐 2. Extract Content from Webpages

The script visits each search result and downloads the webpage using requests.get().

It then parses the HTML content using BeautifulSoup to extract headings (h1, h2, h3), paragraphs (p), and links (a).

📂 3. Categorization Based on Keywords

The extracted text is categorized into predefined themes:

Market Trends → If text contains "trend," "growth," "future," or "forecast 

Strategy → If text contains "strategy," "business model," or "plan."

Finance → If text contains "investment," "funding," "revenue," or "profit."

Competition → If text contains "competitor," "market share," or "industry leader."

General → If no specific category is matched.

This categorization helps consultants analyze trends and strategies easily.

📊 4. Data Storage

The extracted and categorized data is stored in a CSV file (consulting_market_analysis.csv) for further analysis.

The CSV file contains 5 columns:

Website → The URL of the scraped page

Tag → HTML tag of extracted content (h1, h2, p, etc.)
Content → Extracted text
Link → Any hyperlinks found
Category → The assigned category (Market Trends, Strategy, Finance, etc.)
🛑 5. Handling Errors & Rate Limits
If a website fails to load, the script catches the error and continues.
It includes a 2-second delay (time.sleep(2)) between requests to avoid being blocked by websites.
