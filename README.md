# Spotify: What Makes a Free User Pay?



**Question:** Which free Spotify users are most likely to upgrade to Premium, and what should the product do about it? [Independent portfolio project, not affiliated with Spotify ]



**Data:** Survey of 520 Spotify users (India pricing). Analysed in SQL (SQLite), with a revenue model in Google Sheets and a sample-size calculation in Python. Public survey dataset from [source], not collected by me

> This is survey data, not usage logs. It shows which kinds of users are more likely to say they'd pay. It cannot measure retention or real conversion.



## Key findings

1. **Podcast-first free users are the warmest leads.** 54.8% say they'd pay for Premium, versus 21.1% of music-first users (about 2.6x).
2. **Conversion peaks mid-life, not at sign-up.** Only 7.7% of users in their first 6 months are on Premium, versus 22-23% at 6 months to 2 years. Willingness among free users peaks at 38.0% for 6-12 month users.
3. **A surprising result did not hold up.** Users who rated recommendations a 2 were the most willing to pay (43.3%). But 39% of low raters are podcast-first (vs 15% of everyone else). Among music-first users alone, the gap nearly disappears (24.0% vs 20.9%).
4. **Podcast and music users want different plans.** Podcast-first warm leads lean toward Duo (47.5%); music-first lean toward Individual (34.3%) and Student (31.4%). Small group (n = 40), so directional.



## Recommendation

Test a podcast-focused Premium prompt for free podcast listeners.

* **Hypothesis:** a prompt built around podcast benefits lifts 30-day free-to-Premium conversion from an assumed 5% to 7%.
* **Primary metric:** 30-day free-to-Premium conversion.
* **Guardrail:** 30-day free-user retention.
* **Sample size:** 2,213 users per group (4,426 podcast listeners), which needs a pool of about 26,000 free users.
* **Size of prize:** about Rs 3.98 lakh to Rs 11.94 lakh per year per 10,000 free users, depending on how many willing users actually convert (10-30%). Illustrative; assumptions are flagged in the model.

Full detail in `product brief.pdf`.



## Limits

* Survey data, so stated intent overstates real behaviour.
* Sample skews female and aged 20-35, so it is not representative of all Spotify users.
* Several groups are small (radio-only n = 51, podcast warm leads n = 40).
* Tenure groups are different people, not the same people tracked over time.
* The 5% baseline conversion in the test design is an assumption.

## Files

- `analysis.sql`: 15 SQL queries, including a CTE and window functions
- `sample_size.py`: A/B test sample-size calculation
- `revenue_model.png`: screenshot of the Google Sheets revenue model
- `product_brief.pdf`: one-page product brief
- `Spotify_data.csv`: source survey data
|`Spotify\_data.csv`|Source survey data|

## Tools

SQL (SQLite), Python (scipy), Google Sheets

