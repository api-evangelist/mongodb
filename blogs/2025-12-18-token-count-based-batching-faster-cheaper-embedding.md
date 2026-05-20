---
title: "Token-count-based Batching: Faster, Cheaper Embedding Inference for Queries"
url: "https://www.mongodb.com/company/blog/engineering/token-count-based-batching-faster-cheaper-embedding-inference-for-queries"
date: "Thu, 18 Dec 2025 15:00:00 GMT"
author: ""
feed_url: "https://www.mongodb.com/blog/rss/"
---
Embedding model inference often struggles with efficiency when serving large volumes of short requests—a common pattern in search, retrieval, and recommendation systems. At Voyage AI by MongoDB, we call these short requests queries, and other requests are called documents. Queries typically must be served with very low latency (typically 100–300 ms).
