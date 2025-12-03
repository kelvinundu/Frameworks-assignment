# Frameworks-assignment
Findings Report
The analysis, based on the simulated CORD-19 research metadata (filtered for 2020-2022 by default), reveals clear patterns typical of a public health crisis:

Temporal Trend: The Line Chart shows a rapid increase in the number of publications in 2020 and 2021 (the initial crisis years), peaking and slightly tapering off by 2022 as the focus shifted from foundational research to long-term impact.

Top Journals: High-impact medical journals like The Lancet, NEJM, and Nature Medicine dominate the research publication count, indicating the critical, high-profile nature of the work.

Source Distribution: The bulk of the research originates from PMC (PubMed Central) and WHO (World Health Organization) databases, reflecting the institutional nature of global health research dissemination.

Title Keywords: The most frequent words in the titles (e.g., 'coronavirus', 'vaccine', 'health', 'wuhan') directly correlate with the central themes of the pandemic.

Reflection on Challenges and Learning

Challenge: Streamlit Integration: Ensuring the entire workflow (data loading, cleaning, filtering, and plotting) executes correctly within the reactive environment of Streamlit was key. Using the @st.cache_data decorator was crucial for performance, ensuring the large synthetic dataset is generated only once, even if the user interacts with the sidebar widgets multiple times.

Learning: Data Preparation: The necessity of handling missing data (e.g., dropping rows with no title, filling missing abstracts with '') and converting the publish_time column to a proper datetime object highlights that data cleaning is the single most important step before any meaningful analysis can begin.


This single file, app.py, can be run by the user via the command streamlit run app.py and provides a functional, interactive data analysis application.
