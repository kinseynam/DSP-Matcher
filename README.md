[README.md](https://github.com/user-attachments/files/35112180/README.md)
# DSP Business Brother Matcher

A simple web tool for Duke's Delta Sigma Pi chapter that pairs each new member (NME class) with a junior Business Brother based on shared career interests.

**Live site:** https://YOUR-USERNAME.github.io/dsp-matcher/

## What it does

The Business Brother Program matches every new member with a junior who shares their career interests. Big-little stays social; Business Brothers are for career guidance. This tool takes the responses from the matching Google Form and suggests the best pairs.

- **Load responses:** upload the Google Form's CSV, or paste rows straight from the responses Google Sheet
- **Automatic matching:** finds the best overall set of pairs, not just first-come pairings
- **Fair load:** every junior gets one new member before anyone gets a second (the limit per junior is adjustable)
- **Manual overrides:** change any pair with a dropdown
- **Export:** copy the pairs into Google Sheets, or as text for an announcement

## How to use it

1. Open the Google Form → **Responses** tab → **Link to Sheets**
2. In the sheet: **File → Download → Comma-separated values (.csv)**
3. Open the live site and click **Upload CSV**
4. Review the pairs, adjust any by hand, then click **Copy pairs for Google Sheets**

Click **Try with sample data** to see how it works with made-up names.

## How pairs are scored

| Signal | Points |
|---|---|
| Same top career interest | +10 |
| Junior checked the new member's top interest | +5 |
| New member checked the junior's top interest | +3 |
| Each career path both people checked | +2 |
| Similar major | +1 |

## Expected form questions

The tool looks for these questions in the header row (the wording can vary slightly):

- Email Address
- Full name *(required)*
- I am a... → `NME class member` or `Junior brother` *(required)*
- Intended or declared major(s)
- Which career paths interest you? (Select all that apply)
- If you had to pick one, which path is your top interest? *(required)*
- Anything else that would help us find a good match? (Optional)

If someone submits the form twice, only their latest response is used.

## Privacy

Everything runs in your browser. Responses are never uploaded or stored, so no member data is saved to this repo or anywhere else.

## Updating the site

Edit or replace `index.html` in this repo. GitHub Pages republishes within a few minutes.
