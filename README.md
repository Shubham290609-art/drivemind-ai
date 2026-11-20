# 🧠 DriveMind AI: Real-Time Marketplace Brain

A multi-agent assistant for ride-share/delivery drivers that suggests optimal positioning based on live demand forecasting, with built-in safety fallbacks for stale models or sudden events.

## 🏆 Hackathon Rubric Alignment
1. **Working Demo**: Live FastAPI backend + interactive frontend.
2. **Innovation**: Multi-agent routing (Forecaster Agent + EventGuard Agent + Fallback Agent).
3. **Measured Result**: Baseline idle time = 12m. DriveMind target = <8m (32% improvement shown in UI).
4. **Reliability/Safety**: Explicitly handles "Stale Model" and "Stadium Surge" edge cases via the Judge Control Panel.

## 🚀 How to Run Locally
1. Install dependencies: `pip install -r requirements.txt`
2. Run the server: `uvicorn app:app --reload`
3. Open your browser: `http://localhost:8000/static/index.html`

## 🎯 Demo Script for Judges
1. Show the normal flow: Click "Get Next Location" → Agent gives ML recommendation.
2. Click **"Inject Stale Model"** in the Judge Panel → Click "Get Next Location" → Show the **Fallback Safety Agent** gracefully taking over.
3. Click **"Trigger Stadium Exit"** → Show the **EventGuard Agent** proactively redirecting the driver to avoid traffic and capture surge pricing.
