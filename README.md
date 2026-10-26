# Pronto App Review Analysis

I analyzed public Google Play reviews of the Pronto house-help app to find out what unhappy customers complain about the most.

*This is a personal learning project. I used only public Play Store reviews, and I am not affiliated with Pronto.*

## What I wanted to find out

What do customers complain about in 1-2 star reviews, and is it getting better or worse over time?

## Data

- **Source:** Public Google Play Store reviews of Pronto, collected with the `google-play-scraper` Python library
- **Size:** [X] reviews from [start date] to [end date]
- **What I kept:** only the review text, star rating and date. I did not save usernames or any personal data.

## How I did it

1. Downloaded the newest reviews and saved them in a CSV file.
2. Cleaned the text (made it lowercase, handled empty reviews) and converted the dates.
3. Marked reviews with 1-2 stars as **negative**.
4. Made keyword lists for each complaint theme: cancellation, refund/money, support, late/delay, quality, pricing, trust/fraud, app bug and no-show.
5. Calculated what percentage of negative reviews mention each theme, overall and month by month.
6. Checked how often cancellation complaints also mention refunds or support.
7. Read a random sample of reviews myself to check that my keywords work properly.

## What I found

1. **Cancellation is the most common complaint.** About [X]% of negative reviews mention it, and the share is [steady / changing] from [month] to [month].
2. **Cancellation complaints often involve money.** [X]% of cancellation reviews also mention refunds or money, compared with [Y]% of all negative reviews.
3. **Quality and pricing are rarely mentioned** ([X]% and [Y]%). So the main problem seems to be reliability and how issues are handled, not the cleaning itself.

![Themes in negative reviews](themes.png)
![Negative reviews by month](monthly_negative.png)

## Ideas for the product

- Tell customers early when no professional is available, and offer to rebook automatically instead of cancelling at the last minute.
- Make refunds or credits for cancelled bookings quick and easy to see in the app.
- Make sure support can actually solve the problem, not only reply.

## Limitations

- I only used Play Store reviews from about [N] months. No App Store data.
- Unhappy customers are more likely to write reviews, so these numbers describe reviewers, not all customers.
- Keyword matching is rough, so the percentages are approximate.
- Calling 1-2 star reviews "negative" is a simple rule.

## What I want to do next

- Try a sentiment or topic model instead of keywords and compare the results.
- Add App Store reviews and one or two competing apps.
- Build a small professional-to-booking matching prototype using synthetic data.

## How to run it

```
pip install google-play-scraper pandas matplotlib
```

Open the notebook and run all the cells. The first run downloads the reviews, and later runs reuse the saved CSV.

## Tools used

Python, pandas, matplotlib, google-play-scraper, Jupyter Notebook

## About me

Poorna Chandrika, B.E. CSE (AI & ML), Stanley College of Engineering and Technology for Women, Hyderabad
GitHub: [your GitHub link] | LinkedIn: [your LinkedIn link]
