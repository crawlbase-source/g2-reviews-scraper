# g2-reviews-crawler

Welcome to the Crawlbase G2 Reviews Scraper project! This project showcases how to scrape G2 product reviews using Crawlbase, Firebase, ExpressJS, and Cheerio. It's a step-by-step guide to extracting valuable review data efficiently. Let's dive into the details:

Installation:

Before you begin, ensure you have Node.js installed. Then, run the following command in your terminal to install the required packages:

`npm i`

Setting Up Firebase:

Make sure you have a Firebase project set up. Obtain the service account key and replace path/to/serviceAccountKey.json with its path. Also, update the databaseURL with your Firebase URL.

Scraping with Crawlbase:

We're using Crawlbase's Crawling API to get the HTML of the G2 product reviews page. Replace "USER_TOKEN" with your Crawlbase Normal token.

Parsing HTML with Cheerio:

The parsedDataFromHTML function uses Cheerio to extract relevant data from the HTML. It gathers product name, star ratings, total reviews, reviewer details, and more.

Express App Setup:

We've set up an Express app to create an endpoint at /scrape. This endpoint triggers the scraping process and data storage in Firebase.

Scraping and Storing Data:

When a GET request is made to /scrape with the url parameter, the Crawlbase API fetches the HTML. The extracted data is then parsed using Cheerio and stored in the Firebase Realtime Database.

Running the Server:

To run the server, execute:

`node app.js`

The server will start on port 3000, and you can access the /scrape endpoint.

This project guides you through a complete process of scraping G2 product reviews, parsing the data, and storing it in Firebase. Remember to replace placeholders with your own tokens, URLs, and paths. Feel free to customize the project according to your needs. Happy scraping!
