---
title: "Towards Model-based Verification of a Key-Value Storage Engine"
url: "https://www.mongodb.com/company/blog/engineering/towards-model-based-verification-key-value-storage-engine"
date: "Fri, 27 Feb 2026 15:30:00 GMT"
author: ""
feed_url: "https://www.mongodb.com/blog/rss/"
---
In our previous post, we talked about our process of specifying MongoDB’s distributed transactions protocol and how it enabled novel analysis of its performance characteristics. In this follow-up, we talk about how the modularity of our specification also enabled us to check that the underlying storage engine implementation actually conforms to the abstract behavior defined in our formal specification. That is, we are able to formalize the interface boundary between the sharded transaction protocol and WiredTiger, the underlying key-value storage engine, and develop an automated way to…
