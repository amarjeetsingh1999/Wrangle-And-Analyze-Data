# Wrangle-And-Analyze-Data
![](thumbnail.PNG)
## Overview
Real-world data rarely comes clean. Using Python and its libraries, i gathered data from a variety of sources and in a variety of formats, assessed its quality and tidiness, then cleaned it. This is called data wrangling. I documented the wrangling efforts in a Jupyter Notebook, plus showcased them through analyses and visualizations using Python (and its libraries) and/or SQL.

The dataset that was wrangled (and analyzed and visualized) is the tweet archive of Twitter user [@dog_rates](https://twitter.com/dog_rates), also known as [WeRateDogs](https://en.wikipedia.org/wiki/WeRateDogs). WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "[they're good dogs Brent](http://knowyourmeme.com/memes/theyre-good-dogs-brent)." WeRateDogs has over 4 million followers and has received international media coverage.

## Context
My goal: wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information. Additional gathering, then assessing and cleaning is required for "Wow!"-worthy analyses and visualizations.

## The Data

### Enhanced Twitter Archive
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which was used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, it was filtered for tweets with ratings only (there are 2356).
This data was extracted programmatically, but not very well. The ratings weren't all correct. Same goes for the dog names and probably dog stages too. It was required to assess and clean these columns if I wanted to use them for analysis and visualization.

### Additional Data via the Twitter API
Back to the basic-ness of Twitter archives: retweet count and favorite count are two of the notable column omissions. Fortunately, this additional data can be gathered by anyone from Twitter's API. Well, "anyone" who has access to data for the 3000 most recent tweets, at least. But I, because I had the WeRateDogs Twitter archive and specifically the tweet IDs within it, gathered this data for all 5000+. I queried Twitter's API to gather this valuable data.

### Image Predictions File
One more cool thing: Every image in the WeRateDogs Twitter archive was ran through a neural network that can classify breeds of dogs*. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).

## Steps Followed
- Data wrangling, which consists of:
  - Gathering data
  - Assessing data
  - Cleaning data
- Storing, analyzing, and visualizing the wrangled data
- Reporting on 1) data wrangling efforts and 2) data analyses and visualizations

### Reports
- [Wrangle Report](wrangle_report.pdf)
- [Act Report](act_report.pdf)

## Technologies and Tools Used
- Jupyter Notebook
- Python, NumPy, pandas
- requests, tweepy, json
- Matplotlib, seaborn
