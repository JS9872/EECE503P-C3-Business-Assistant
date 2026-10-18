# C3 demo recording guide

1. In this folder, run `python app.py` and open the printed local URL.
2. Ask: `What services do you offer?` Show that the reply uses the published business profile.
3. Ask: `I am interested in math tutoring. My name is Demo Student and my email is demo@example.com.` Show the lead reply, then open `logs/leads.jsonl` to show the saved record.
4. Ask: `What is the exact hourly price?` Show the unknown-price reply, then open `logs/feedback.jsonl` to show the logged question.
5. Briefly show the separately labeled `PERSONA`, `INSTRUCTIONS`, router, and tool schemas in `app.py` or `business_agent.ipynb`.

The free Gemini tier can pause with a quota message. Wait about a minute before retrying. Use only sample contact details in the recording.
