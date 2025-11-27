
# 📺 YouTube Video Explainer

This project is an AI-powered tool that takes any YouTube video URL, extracts its content, and generates a structured, educational summary. Powered by **Google's Gemini 2.0 Flash** model, it turns video subtitles into high-quality study notes, step-by-step guides, and code snippets.

## ✨ Features

* **Automated Transcript Extraction:** Fetches subtitles directly from YouTube videos using the transcript API.
* **Smart Summarization:** Generates a structured breakdown including:
    * **Overview:** A concise summary of the video's topic.
    * **Key Concepts:** Fundamental ideas explained clearly.
    * **Deep Dive:** A detailed explanation of the subject matter.
* **Tutorial Detection:** Automatically detects if a video is a tutorial and generates a **Step-by-Step Guide**.
* **Code Extraction:** For programming videos, it extracts and formats **Code Snippets** with comments and explanations.
* **Interactive UI:** Built with **Gradio** for a clean, user-friendly web interface.

## 🛠️ Tech Stack

* **Python 3**
* **Google Gemini API** (LLM for summarization)
* **YouTube Data API & Transcript API** (Data extraction)
* **Gradio** (User Interface)

---

## 🚀 How to Run Locally

Follow these steps to set up the project on your local machine.

### 1. Prerequisites

Ensure you have Python installed (version 3.10 or higher is recommended).

### 2. Install Dependencies

1.  Ensure you have the `requirements.txt` file in your project directory.
2.  Run the following command in your terminal to install all required libraries:

```bash
pip install -r requirements.txt
````

### 3\. 🔑 API Key Configuration (Crucial Step)

This project requires two API keys to function. You must store these in a `.env` file to keep them secure.

**Step A: Get the API Keys**

1.  **Gemini API Key:**
      * Go to [Google AI Studio](https://aistudio.google.com/app/apikey).
      * Click "Create API key" and copy the string.
2.  **YouTube Data API Key:**
      * Go to the [Google Cloud Console](https://console.cloud.google.com/).
      * Create a new project (or select an existing one).
      * Search for "YouTube Data API v3" in the library and enable it.
      * Go to "Credentials" → "Create Credentials" → "API Key".

**Step B: Create the Environment File**

1.  Create a new file in the root directory of the project named `.env`.
2.  Paste your keys into the file using the exact format below:

<!-- end list -->

```env
GEMINI_API_KEY=your_gemini_api_key_here
YOUTUBE_API_KEY=your_youtube_api_key_here
```

*(Note: Do not wrap the keys in quotes. Just paste the raw text after the `=` sign).*

### 4\. Running the Application

1.  Open the `VideoExplainer.ipynb` file in **Jupyter Notebook**, **JupyterLab**, or **VS Code**.
2.  Run all the cells in order.
3.  The last cell will launch the Gradio interface. You will see an output similar to:
    ```
    Running on local URL:  [http://127.0.0.1:7863](http://127.0.0.1:7863)
    ```
4.  Click the local link to open the summarizer in your browser.

-----

## 📝 Usage

1.  Copy the URL of a YouTube video (e.g., a coding tutorial, a lecture, or a documentary).
2.  Paste the URL into the **"Paste YouTube Video URL"** box in the app.
3.  Click **"Summarize 🚀"**.
4.  Wait a few seconds for Gemini to process the transcript.
5.  Read your structured notes, copy the code snippets, and enjoy learning\!
