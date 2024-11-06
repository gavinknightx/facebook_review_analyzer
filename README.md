# Facebook Reviews Analyzer
A comprehensive tool for analyzing Facebook business profile reviews using AI-powered sentiment analysis and natural language processing. This project helps businesses understand customer feedback through automated analysis of their Facebook reviews.

## 📁 Project Structure
```
.
├── api
│   ├── analyze.py
│   ├── api.py
│   ├── config
│   │   ├── **init**.py
│   │   ├── llm_config.py
│   │   ├── prompts.py
│   │   └── tokens.json
│   ├── data
│   │   └── reviews.json
│   ├── fb_reviews.py
│   └── **init**.py
├── app
│   └── app.py
└── requirements.txt
```

## 🛠️ Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/gavinknightx/facebook_review_analyzer.git
   cd facebook-reviews-analyzer
   ```

2. Create and activate a Python virtual environment:
   
   For Windows:
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```
   
   For macOS/Linux:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Install additional required packages:
   ```bash
   pip install uvicorn streamlit
   ```

4. Add your OpenAI API key to `.env` file in the root directory:
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

3. If you encounter any dependency-related errors, ensure that both Uvicorn and Streamlit are properly installed by running:
   ```bash
   pip install uvicorn streamlit
   ```
   These packages are essential for running the backend API server and frontend interface respectively.

## 📱 How to Use
1. Navigate to the web interface that opens in your browser after starting the Streamlit frontend.

2. You can analyze reviews for supported companies by typing phrases like:
   ```
   "Analyze reviews for Dialog"
   ```

3. Currently supported companies:
   - Dialog
   - SLT
   - Elephant House


## 🔧 Configuration
- Configure LLM settings in `api/config/llm_config.py`
- Adjust prompts in `api/config/prompts.py`
- Update token configurations in `api/config/tokens.json`
