# C3 - Agent-Powered Business Assistant

**Joey Saade - 202305993**

The fictional Harborlight Learning Studio chatbot answers from its profile, routes questions, collects leads, and logs unanswered questions. The persona and operating instructions are separately labeled in `app.py` and `business_agent.ipynb`.

## Run

1. Install: `python -m pip install -r requirements.txt`
2. Get a free-tier key from [Google AI Studio](https://aistudio.google.com/app/apikey). Copy `.env.example` to `.env` and replace `replace_with_your_key` with the key. Do not commit `.env`.
3. Run `python app.py` and open the local Gradio URL.
4. Try: "What services do you offer?", "I am interested in math tutoring; my name is Joey and my email is joey@example.com", and "What is your exact hourly price?".
5. Inspect `logs/leads.jsonl` and `logs/feedback.jsonl` to verify tool calls.

`app.py` uses the Gemini API through the `google-genai` SDK. Its router runs before the model and records one of three intents. The model may then request an allowed tool; Python executes it and sends the observation back to the model. The business is fictional; its contact address is illustrative.

To deploy on Hugging Face Spaces, create a Gradio Space, upload this folder's contents except `.env` and `logs`, and set `GEMINI_API_KEY` as a Space secret. Set the Space app file to `app.py`. The assignment requires a GitHub repository and demo video; those external artifacts require publishing and recording from an account.
