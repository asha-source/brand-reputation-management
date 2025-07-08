# brand-reputation-management

COMPANY:CODTECH IT SOLUTIONS

NAME:NASINA ASHALATHA

INTERN ID:CT08DN658

DOMAIN:DIGITAL MARKETING

DURATION:8WEEKS

MENTOR:NEELA SANTHOSH KUMAR

DESCRIPTION:

Code Description: Brand Reputation Management
✅ Purpose:
This code helps analyze customer reviews and identify whether they are positive, negative, or neutral. It's a basic tool to manage a brand's online reputation by understanding public sentiment.

🔍 Libraries Used:
Library	Purpose
requests	(Prepared for fetching web content – not used here)
BeautifulSoup	(Also prepared for scraping – not used directly in this demo)
TextBlob	To analyze the sentiment polarity of text (positive/negative)
pandas	To organize the data and save it into a .csv file

🧠 Step-by-Step Code Breakdown
1. Simulated Customer Reviews
python
Copy code
sample_reviews = [...]
A list of sample customer reviews is created. These simulate what real user reviews might look like.

2. Sentiment Analysis
python
Copy code
for review in sample_reviews:
    sentiment = TextBlob(review).sentiment.polarity
TextBlob calculates sentiment polarity:

Ranges from -1.0 (very negative) to +1.0 (very positive)

python
Copy code
sentiment_type = "Positive" if sentiment > 0 else "Negative" if sentiment < 0 else "Neutral"
Based on the score:

0 → Positive

< 0 → Negative

== 0 → Neutral

3. Store Sentiment Results
python
Copy code
results.append({...})
Each review is stored along with:

Its sentiment label (Positive/Negative/Neutral)

The sentiment score

4. Create DataFrame
python
Copy code
df = pd.DataFrame(results)
Creates a table-like format from the collected data for easy reading and export.

5. Save to CSV File
python
Copy code
df.to_csv("brand_sentiment_report.csv", index=False)
Saves the results to a file named brand_sentiment_report.csv, which you can open in Excel or Google Sheets.

6. Display Results
python
Copy code
print(df)
Prints a readable summary in the console showing each review and its sentiment.

✅ Example Output (Printed on Screen):
mathematica
Copy code
Brand Reputation Summary:

                                             Review  Sentiment  Score
0    Amazing service and very helpful staff!   Positive    0.75
1  Terrible experience. The support team was very rude.  Negative   -0.90
2                    I love their fast delivery!   Positive    0.50
3   The product quality is bad and not worth the price.  Negative   -0.60
4                Very satisfied with my purchase.   Positive    0.55
5       Customer care is the worst. Not helpful at all.  Negative   -0.85
📁 File Created:
brand_sentiment_report.csv — Can be submitted as a part of your deliverable.

🔚 Summary:
This code offers a basic but effective way to:

Monitor public sentiment

Detect negative reviews

Build a data-driven reputation strategy

output:

[brand_sentiment_report.csv](https://github.com/user-attachments/files/21126374/brand_sentiment_report.csv)
