<!-- njnmdoc: title="google sheets tips" -->


from: https://twitter.com/Morchickit/status/1331341641114902529


THREAD  - this evening I gave a talk
@opendatamcr
 Pick 'N Mix on Tips and Tricks for Google Sheets, so I am sharing it here too. These are about product functions that are unique to Google, and not advanced analysis methods. Let's dig in!
@googledocs

Tip 1a. You can import many data formats directly to sheets using functions. Google in some cases also save you time on scrapping data. Try the IMPORTHTML to import a table from a webpage or IMPORTFEED to get and RSS or ATOM feed directly to a spreadsheet https://support.google.com/docs/answer/3093339

Tip 1b. You can also directly import .csv or .xls from the web to sheets using the IMPORTDATA or connect to a range in another google sheet by using IMPORTRANGE. It saves a lot of copy paste work and connects work together. https://support.google.com/docs/answer/3093340

Tip 2. Google created functions that you can use with it's different services. Try GOOGLEFINANCE to get exchange rate https://support.google.com/docs/answer/3093281?hl=en.
DETECTLANGUAGE to figure out what languages are used in the sheet and then GOOGLETRANSLATE to it for analysis https://support.google.com/docs/answer/3093331?hl=en.

Tip 3. You can create a Google form directly from Google sheets and then get the responses to the same sheet. Just go to Tools -> Create a Form.

Tip 4a. You can make Google Sheets into an SQL dataset using the QUERY functions. Very powerful for some language analysis that can not be done with Sheets functions. Google Query language is very similar to SQL so easy to learn. https://support.google.com/docs/answer/3093343?hl=en-GB


4b. Some shameless plug here for an analysis I did using the QUERY function in Sheets for @360Giving.  Analysing grants for LGBTQI+ organisations - 360Giving
The end of June was a time of pride. Rainbow flag To help mark it, I analysed 360Giving data to understand grants made to LGBTQI+ causes.  It was also a good excuse to use some of the new principles I...
threesixtygiving.org

Tip 5. Google allows you to publish to the web and make your spreadsheet an engine behind a website or allow more than 100 users to access it. Just makr sure there is no sensitive data on your sheet before publishing! https://support.google.com/a/users/answer/9308870?hl=en

Tip 6. Use Google Explore tool. Look at the right lower side of your spreadsheet, this is where you find it. It helps to explore datasets in seconds and analyse the dataset without writing a single function. Magic!
Analyze easily with Explore in Sheets
Jimmy and Lily discuss Explore in Sheets to help you decipher your data easily. They take a look at our team stats and walk through a data dump and turn it i...
youtube.com

Tip 7. You can create awesome dashboards by connecting your Google Sheet to Google Data Studio and master your visualisations skills even further! https://support.google.com/datastudio/answer/6283323?hl=en

I believe that 80% of data analysis (if not more) can be done in spreadsheets. Take time to explore, learn and play with Google Sheet to see if it works for your data needs. You can also subscribe to Google Workplace updates here - https://cloud.google.com/blog/products/workspace cc
@TGyateng
