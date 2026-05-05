---
title: "Enhance Your In-IDE Data Browsing Experience With MongoDB"
url: "https://www.mongodb.com/company/blog/technical/enhance-your-in-ide-data-browsing-experience-with-mongodb"
date: "Tue, 17 Mar 2026 17:00:00 GMT"
author: ""
feed_url: "https://www.mongodb.com/blog/rss"
---
<p>MongoDB is excited to announce the general availability of our enhanced data browsing experience in the MongoDB for Visual Studio (VS) Code extension. This new experience offers a unified workspace for developers to visually browse, query, and edit their data natively, streamlining workflows so they can manage their database right where they write their code.</p>
<p>Evolving the developer workflow
The modern developer’s workflow is incredibly fast-paced. With developers juggling an average of 14 different tools daily, the cognitive load of constantly jumping between applications can easily disrupt focus. When your application needs to evolve, working with your data shouldn’t force a break in your flow state.</p>
<p>As the MongoDB for VS Code extension has grown to nearly 3 million downloads, we’ve seen firsthand how developers are pushing the boundaries of what an in-IDE (integrated development environment) database tool can do. While developers love accessing their data directly in the editor, we wanted to transform this experience to be even more visual, actionable, and seamless. Instead of switching to external terminals for quick tasks or taking the time to translate familiar MongoDB Shell commands into Extended JSON (EJSON), we are bringing a full-fledged, intuitive data management suite right to your VS Code sidebar.</p>
<p>Exploring what’s new in the MongoDB for VS Code extension
Here are the key improvements that transform the extension into a complete workflow solution:</p>
<ol>
<li>Paginated tree view and prescriptive titles
Understanding complex data models at a glance is crucial for rapid development. We are transforming the document browsing experience by automatically detecting human-readable fields (like names or emails) to create prescriptive document titles, rather than just displaying standard _id hashes. Furthermore, you can now use a structured, paginated tree view to instantly browse collection data from the “Documents” tab, as well as interactively explore playground results when you run a script. This means you get the full context of your collections visually and instantly.</li>
</ol>
<p>Figure 1. Paginated tree view and prescriptive titles</p>
<ol start="2">
<li>Powerful action menus and header controls
Navigating your data should be inherently actionable. To give you full management capabilities without the need for you to write manual queries, we’ve added a new action header directly inside the tree view. This header equips you with buttons to instantly insert documents, refresh (to rerun the current query or playground script), sort ascending/descending by _id, paginate through results, and even bulk delete to empty a collection.</li>
</ol>
<p>Additionally, managing individual records is easier than ever. Simply hover over any document within the tree view to reveal a contextual action menu that allows you to instantly delete, copy, clone, and edit the document natively.</p>
<p>Figure 2. Native action menus</p>
<ol start="3">
<li>Native editing and shell syntax default
We wanted to make interacting with your database as natural as possible.</li>
</ol>
<p>To remove the friction of translating your commands, we’ve added a setting that defaults to standard Shell syntax over EJSON for all insert, clone, edit, and clipboard functionalities. This guarantees that any document you copy or any quick fix you make in the extension is instantly compatible with your application code.</p>
<p>Figure 3. Clone action.</p>
<p>Stop context switching and start building
Your database tools should adapt to your workflow, not disrupt it. By bringing native data editing, intelligent tree views, and standard Shell syntax directly into your sidebar, we’re bridging the gap between writing code and managing data. You no longer have to sacrifice your flow state just to make a quick database fix, verify a playground result, or translate verbose EJSON formats. This overhaul is another step in our commitment to making this MongoDB extension your ultimate command center—empowering you to spend less time wrestling with external tools and more time actually building your application.</p>
