1. FlyRank — Content Decline Prioritization
The Problem

SEO and content teams manage large numbers of pages, but not every page showing declining performance deserves attention at the same time. I wanted to build a way to prioritize which content pages were worth investigating or refreshing first using search-performance data.

The Data

I worked with the FlyRank/internship-warehouse dataset, containing anonymized Google Search and engagement data. I created 90-day features and compared the most recent 45 days with the previous 45 days.

Some of the features included previous-period impressions, visible queries, query-share signals, and search-position volatility.

The Approach

I built a Random Forest classifier to rank pages based on their likelihood of showing a meaningful decline in search performance.

I evaluated the model using a held-out split grouped by client, keeping clients in the test set separate from those used for training.

Results

The model achieved:

Precision@50: 0.680
Baseline: 0.380

This means the model was substantially better at identifying useful pages to investigate within the top 50 recommendations than the baseline approach.

What I Built

The output is a prioritized list of pages, rather than an automatic decision to refresh content. A content team could use the ranking to investigate the highest-priority pages first.

The next step is to turn this ranking into a simple CSV output containing the page, decline score, performance changes, and priority rank.

What I Learned

The project taught me that building a model is only part of the problem. A useful ML system also needs to turn its predictions into something that a person can actually act on.
