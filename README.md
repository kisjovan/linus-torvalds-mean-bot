# Linus Torvalds Mean Bot

This is a Chainlit-powered chatbot that mimics Linus Torvalds' "mean" style using the Grok (xAI) LLM. It is designed to be embedded as a Copilot in a website.

## Setup

1.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

2.  **Environment Variables:**
    Copy `env.example` to `.env` and add your xAI API Key.
    ```bash
    cp env.example .env
    # Edit .env and set XAI_API_KEY
    ```

3.  **Run the Chainlit Server:**
    ```bash
    chainlit run app.py -w
    ```
    The `-w` flag enables auto-reloading.

## Embedding (Copilot)

To see the chatbot embedded in a website:

1.  Make sure the Chainlit server is running (default: `http://localhost:8000`).
2.  Open `index.html` in your browser.
    *   **Note:** For the Copilot to work correctly, `index.html` usually needs to be served by a web server (due to CORS/browser restrictions), though sometimes it works locally.
    *   You can serve it easily with python:
        ```bash
        python -m http.server 8001
        ```
    *   Then go to `http://localhost:8001`.

## Customization

*   **Mean Emails:** Edit the `MEAN_EMAILS_CONTEXT` variable in `app.py` to add the actual content of the emails you want the bot to use as reference.
*   **Model:** The code is configured to use `grok-beta`. Change the `model` parameter in `app.py` if needed.


