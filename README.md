# Facebook Reviews Analyzer

A comprehensive tool for analyzing Facebook business profile reviews using AI-powered sentiment analysis and natural language processing. This project helps businesses understand customer feedback through automated analysis of their Facebook reviews.

## 📁 Project Structure

```
.
├── api
│   ├── analyze.py
│   ├── api.py
│   ├── config
│   │   ├── __init__.py
│   │   ├── llm_config.py
│   │   ├── prompts.py
│   │   └── tokens.json
│   ├── data
│   │   └── reviews.json
│   ├── fb_reviews.py
│   └── __init__.py
├── app
│   └── app.py
└── requirements.txt
```

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/facebook-reviews-analyzer.git
   cd facebook-reviews-analyzer
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the root directory and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

## 🚦 Running the Application

1. Start the FastAPI backend server:
   ```bash
   cd api
   uvicorn api:app --reload
   ```
   The API will be available at `http://localhost:8000`

2. In a new terminal, start the Streamlit frontend:
   ```bash
   cd app
   streamlit run app.py
   ```
   The web interface will open automatically in your default browser

## 🔧 Configuration

- Configure LLM settings in `api/config/llm_config.py`
- Adjust prompts in `api/config/prompts.py`
- Update token configurations in `api/config/tokens.json`
