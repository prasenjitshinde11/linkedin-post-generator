# LinkedIn Post Generator

A CLI and Streamlit web app that generates LinkedIn posts using Google Gemini API. Takes a topic, tone, audience, length, and copywriting framework as inputs and returns a ready-to-post LinkedIn post.

## How it works

1. User provides a topic, tone, target audience, post length, and copywriting framework
2. A prompt is built using a structured template (`prompt_builder.py`)
3. The prompt is sent to Google Gemini (`gemini-2.5-flash`)
4. The generated post is displayed and can be saved as `.txt`

## Tech Stack

- **Python**
- **Streamlit** — web UI
- **Google Generative AI** — Gemini API for text generation
- **python-dotenv** — environment variable management

## Project Structure

| File | Purpose |
|---|---|
| `app.py` | Streamlit web interface |
| `main.py` | CLI pipeline (topic -> prompt -> generate -> save) |
| `config.py` | Gemini API key loading and model configuration |
| `prompt_builder.py` | Prompt template and post generation logic |
| `user_input.py` | CLI input collection with validation |
| `requirements.txt` | Python dependencies |

## Supported Options

| Parameter | Options |
|---|---|
| **Tone** | Professional, Inspirational, Humorous, Funny, Angry, Sad |
| **Length** | Short (100-150 words), Medium (200-300 words), Long (400-500 words) |
| **Framework** | AIDA, PAS, Storytelling, Listicle, How-to / Tips, None |

## Setup

```bash
pip install -r requirements.txt
```

Create a `.env` file:

```
GEMINI_API_KEY=your_api_key_here
```

## Usage

**Streamlit UI:**
```bash
streamlit run app.py
```

**CLI:**
```bash
python main.py
```
