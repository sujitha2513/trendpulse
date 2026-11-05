# TrendPulse - Part 1: Python Foundations

## How to run
1. Open part1_python_foundations.ipynb in Google Colab.
2. Upload the four CSV files from the data folder to the Colab Files panel.
3. Click Runtime -> Restart session and run all. The notebook runs top to bottom without errors.
Only pandas is needed (already available in Colab).

## Countries and files
- Countries: US, GB, IN
- Files: USvideos.csv, GBvideos.csv, INvideos.csv, categories.csv

## Cleaning rules
- views, likes, dislikes, comment_count are converted to integers.
- Blank likes and comment_count values are set to 0 (only 12 and 36 blanks out of 46,230 records).
- Blank descriptions are set to an empty string.
- comments_disabled, ratings_disabled, video_error_or_removed are converted to booleans.
- trending_date (yy.dd.mm) and publish_time are converted to dates. Parse failures are counted per field with try/except.

## Thresholds
- VIRAL_VIEWS = 1000000
- GOOD_LIKE_RATIO = 0.90
- LOW_VIEWS = 10000
(Used in classify_video. I chose them as simple starting values.)

## Data source
Kaggle - Trending YouTube Video Statistics.
