---
title: "Building a Movie Recommendation Engine with Hugging Face and Voyage AI"
url: "https://www.mongodb.com/company/blog/technical/building-a-movie-recommendation-engine-with-hugging-face-and-voyage-ai"
date: "Tue, 17 Feb 2026 15:30:00 GMT"
author: ""
feed_url: "https://www.mongodb.com/blog/rss"
---
<p>This guest blog post is from Arek Borucki, Machine Learning Platform &amp; Data Engineer for Hugging Face - a collaboration platform for the machine learning community. The Hugging Face Hub works as a central place where anyone can share, explore, discover, and experiment with open-source ML. HF empowers the next generation of machine learning engineers, scientists, and end users to learn, collaborate and share their work to build an open and ethical AI future together. With the fast-growing community, some of the most used open-source ML libraries and tools, and a talented science team exploring the edge of tech, Hugging Face is at the heart of the AI revolution.</p>
<p>Traditional movie search relies on filtering by genre, actor, or title. But what if you could search by how you feel? Imagine typing:</p>
<p>&quot;something uplifting after a rough day at work&quot;</p>
<p>&quot;a movie that will make me cry&quot;</p>
<p>&quot;I need adrenaline, can't sleep anyway&quot;</p>
<p>&quot;something to watch with grandma who hates violence&quot;</p>
<p>This is mood-based semantic search: matching your emotional state to movie plot descriptions using AI embeddings.</p>
<p>In this tutorial, you will build a mood-based movie recommendation engine using three powerful technologies: voyage-4-nano (a state-of-the-art open-source embedding model), Hugging Face (for model and dataset hosting), and MongoDB Atlas Vector Search (for storing and querying embeddings at scale).</p>
<p>Why mood-based search?
Genre tags are coarse. A &quot;drama&quot; can be heartwarming or devastating. A &quot;comedy&quot; can be light escapism or dark satire. Traditional filters cannot capture these nuances.</p>
<p>Semantic search solves this by understanding meaning. When you search for &quot;feel-good movie for a rainy Sunday&quot;, the system doesn't look for those exact words. It understands the intent and matches it against plot descriptions that evoke similar feelings.</p>
<p>Architecture overview
The system combines three components from the Hugging Face ecosystem with MongoDB:</p>
<p>voyage-4-nano (Hugging Face Hub): Converts text to embeddings (up to 2048 dimensions, we use 1024)</p>
<p>MongoDB/embedded_movies(Hugging Face Datasets): 1500+ movies with plot summaries, genres, cast</p>
<p>MongoDB Atlas Vector Search: Stores embeddings and performs similarity search</p>
<p>Understanding voyage-4-nano
voyage-4-nano is the smallest model in Voyage AI's latest embedding series, released with open-weights under the Apache 2.0 license. Voyage AI was acquired by MongoDB, and the Voyage 4 series models are now available through MongoDB Atlas. All models in the series (voyage-4-large, voyage-4, voyage-4-lite, and voyage-4-nano) produce compatible embeddings in a shared embedding space, allowing you to mix and match models within a single use case.</p>
<p>Although voyage-4-nano natively supports embeddings up to 2048 dimensions, we deliberately truncate them to 1024 dimensions using its Matryoshka embedding property. In practice, this provides a strong balance between semantic quality, storage efficiency, and vector search latency, while preserving stable ranking behavior.</p>
<p>Sentence Transformers
This tutorial uses Sentence Transformers, a Python library built on top of Hugging Face Transformers. It is specifically designed for working with embedding models and provides a simple API for generating text embeddings.</p>
<p>Why Sentence Transformers instead of raw Transformers? When working with embedding models, you need to handle tokenization, pooling, normalization, and prompt formatting. Sentence Transformers does all of this automatically in a single method call. The code is cleaner, there are fewer potential errors, and you get built-in features like batch processing with progress bars.</p>
<p>Under the hood, Sentence Transformers still uses Hugging Face Transformers to load and run the model.</p>
<p>Configure the development environment
Let's get started!</p>
<p>Create the Project Structure
Code Snippet
1
mkdir mood-movie-search
2
cd mood-movie-search
3
mkdir src
4
touch requirements.txt .env</p>
<p>Install dependencies
Create the requirements.txt file:</p>
<p>Code Snippet
1
cat &lt; requirements.txt
2
fastapi&gt;=0.109.0
3
uvicorn&gt;=0.27.0
4
pymongo&gt;=4.6.1
5
sentence-transformers&gt;=3.0.0
6
python-dotenv&gt;=1.0.0
7
datasets&gt;=2.16.0
8
torch
9
EOF</p>
<p>Create a Python virtual environment and install dependencies:</p>
<p>to be continued...</p>
