# PocketSmart AI

Complete FastAPI + Jinja2 + SQLite + Gemini implementation based on the supplied PocketSmart AI documentation.

## Included
- Home, Party and Jewelry planners
- Gemini text generation and optional image input
- Offline deterministic fallback when no Gemini key is present
- JWT authentication and recommendation history
- Responsive frontend
- Swagger docs at `/docs`
- Health endpoint at `/api/health`
- Pytest tests

## VS Code
1. Install Python 3.11+.
2. Open this folder in VS Code.
3. Create a venv:
   - Windows: `py -3 -m venv .venv` then `.venv\Scripts\activate`
   - macOS/Linux: `python3 -m venv .venv` then `source .venv/bin/activate`
4. `pip install -r requirements.txt`
5. Copy `.env.example` to `.env`.
6. Put your Gemini API key in `GEMINI_API_KEY` if you want live AI.
7. Run `python run.py`.
8. Open http://127.0.0.1:8000.
9. Register, log in, choose a planner, enter data and generate.
10. Run tests with `pytest -q`.

The source document mentions Gemini 1.5 Flash Pro. The app deliberately makes the model configurable and defaults to `gemini-2.5-flash`, because current Gemini model availability changes over time. It also uses simulated/search links for Amazon, Flipkart, IKEA, Swiggy, Zomato and OYO rather than brittle scraping.
