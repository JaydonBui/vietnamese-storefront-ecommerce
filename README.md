🌐 Vietnamese Storefront Search Relevance Project

Focus: Data-driven search optimization for Vietnamese storefront on Weee!
This is one of the most interesting project that our team is facing and improving.

⚠️ Disclaimer
This project focuses on how we approached search relevance, not on proprietary systems or confidential data. The goal is to show how we think, how we analyze customer behavior, and how we translate those insights into a scalable, data-driven strategy. All examples and metrics are modified or anonymized to comply with data security policies. 

**📌 Introduction**

Weee! is the #1 Asian online grocery in the US, known for serving unique, ethnic-focused products that you rarely find in traditional supermarkets. For Vietnamese consumers in the US, our customer base spans first-generation immigrants, second-generation students, and ethnic shoppers with varying familiarity with Vietnamese foods.
Shopping behavior in ethnic markets is different from mainstream categories. At Weee!, the search box is often the first point of interaction. Customers expect the platform to understand them instantly. When the search fails, trust erodes, they spend more time searching instead of buying, and ultimately GMV and retention are negatively impacted.

This is not like searching for a T-shirt on Amazon 👕. Searching for Vietnamese items in the US is complex. Customers search using:
1. Vietnamese with tones: bò 🥩
2. Vietnamese without tones: bo
3. English: beef

<img width="1910" height="934" alt="image" src="https://github.com/user-attachments/assets/ff3b662e-4187-438a-ad0d-43b04aca06df" />

**❓ Why This Matters**
Imagine walking into a traditional supermarket 🛒. 
There are two types of shoppers: those who know what they want and those who explore. 
The goal of the store owner is to help everyone leave with a full basket 🛍️.
Online, the first step is the search box. When search fails:

⚠️ Customers lose trust:
⏱ They spend more time searching instead of buying

💸 GMV & retention drop

Complexity arises because ethnic items often have ambiguous keywords and multiple ways of writing. Customers try variations, switch languages, and remove tones to find what they need. This persistence signals strong intent 💪, and the system must adapt, not the user.


🔍 What We Observed & Analyzed

We started by understanding how customers search. We mapped keywords to catalog pages and analyzed SEO and discoverability. Our standard title formula:
[Brand] + [Product Type] + [Key Attribute] + [Size/Quantity] + [Optional Flavor/Variant]

We also analyzed no-hit keywords to identify gaps in our catalog.

<img width="464" height="193" alt="image" src="https://github.com/user-attachments/assets/0fa93cd4-aa57-4de6-be7d-adeaee44a19d" />

Before optimization, all categories were displayed equally. High search volume often existed for products that were not searchable, and customers repeatedly tried variations.
Behavioral insights revealed that:

✏️ Users adapt queries (add/remove words)

🔄 Switch languages

❌ Remove tones

-> Persistent behavior signals high intent

**🛠 How We Fixed It – Search Relevance Strategy**

We implemented a Search Relevance Strategy grounded in customer behavior and data.

First thing first. Apply Keyword Normalization & Mapping:

- Handle Vietnamese tone vs flat

- Map Vietnamese ↔ English synonyms

- Group multiple meanings under one normalized keyword

- Example: "bo" → beef, avocado, margarine

-> Rather than guessing intent upfront, behavior clarifies intent:

- Search "bo" → most users add avocado → avocado ranks higher 🥑

- Search "bò" → most users add beef → beef ranks highest 🥩

-> The system continuously learns and updates rankings based on user actions 🔁.

📈 Search Ranking System – Behavioral Data Flow

🔎 User Query: Customer types a query.

📝 Query Preprocessing: Normalize text, detect language, optionally flatten tone.

🔑 Keyword Normalization & Mapping: Map query to all possible SKUs, handle synonyms/multi-language.

📦 Candidate SKU Generation: Pull matching SKUs from catalog with metadata (title, bullets, attributes).

📊 Behavioral Scoring & Ranking: CTR, ATC, CVR, engagement, bounce, seasonality → compute weighted ranking.

🛍 Search Result Display: Present top-ranked SKUs + auto-suggestions / "Did you mean?"

🔁 Feedback Loop / Continuous Learning: Track actions, update behavioral scores, improve keyword normalization & ranking over time.

The pre-display stage retrieves all relevant items and prioritizes high-demand, high-relevance items, letting user behavior clarify intent. Retrieves all relevant items containing “bo” in the product title, vietnamese name or common food phrase, eg:

<img width="682" height="492" alt="image" src="https://github.com/user-attachments/assets/8c860109-03ec-481e-9c6f-2860f5e6e4a3" />

📊 Results & Application

The impact was clear:

+4.8pt YoY improvement in Search Hit Rate (SHR) 📈

SHR consistently >80% vs previous average of 75%

Reduced no-hit searches for high-intent keywords

Improved conversion for ambiguous queries

Better seasonal preparedness for ethnic demand 🎉

This project shows how complex, multi-language customer behavior can be translated into a scalable, data-driven search strategy. The system adapts to the user, improving discoverability, trust, and GMV, while providing actionable insights for catalog, merchandising, and marketing teams.

🔑 Key Takeaways

While the improvements have significantly increased search relevance and user satisfaction, we are still learning and iterating:
User behavior keeps evolving, especially with new arrivals and seasonal products 🥮, so our ranking and normalization models need constant adjustment.
Multi-language searches continue to be challenging, particularly for second-generation and newer immigrant users switching between English and Vietnamese.

No-hit searches for niche products still occur, highlighting the need for continuous catalog expansion and behavioral analysis.
The project reinforced that real user behavior, not assumptions, drives relevance, and ongoing feedback loops are critical to adapt the system as the marketplace grows.

In short: this project is not a one-time fix, but a living system that adapts as customer needs, languages, and seasonal trends evolve.


