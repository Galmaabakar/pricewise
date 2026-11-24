# pricewise
Analytics platform for Trendyol sellers: XGBoost price prediction + Turkish aspect-based sentiment analysis with BERTurk. Next.js · FastAPI · PostgreSQL.

PriceWise is an analytics tool for Trendyol sellers. It combines two ML components:

- **Price prediction**: XGBoost models trained on scraped Trendyol product data (R² ≈ 0.90 on smartphones).
- **Review analysis**: aspect-based sentiment analysis on ~205K Turkish reviews. A lexicon spots the aspects, then a fine-tuned BERTurk model classifies each aspect as positive or negative.

The two outputs feed a product **Health Score** (price 40 % / sentiment 40 % / other 20 %).

**Stack:** Next.js, FastAPI, PostgreSQL (Supabase), Celery, Redis, XGBoost, BERTurk. It doesn't depend on any external LLM API.

Built as a final-year engineering project at Muğla Sıtkı Koçman University.
