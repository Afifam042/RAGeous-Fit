# 👗 Fashion RAG Bot — AI Stylist with Gemini + MongoDB

A Retrieval-Augmented Generation (RAG) chatbot that analyzes natural language queries **and** clothing images to suggest fashion-forward outfit matches. Powered by **Google Gemini**, backed by a **MongoDB** catalog of products, and built to run in **Google Colab** with zero backend setup. Just plug and style! 💫

---

## ✨ Features

- **Gemini Vision Integration**: Understands both text and image context to detect clothing types.
- **MongoDB-Powered Retrieval**: Searches for the best product matches using TF-IDF and cosine similarity.
- **Product-Aware Recommendations**: Suggests complementary pieces based on fashion type (e.g., "top" → recommends "bottom").
- **Image-Based Detection**: Upload a picture, and the bot infers the clothing category automatically.

---

## 🚀 Quick Start (on Google Colab)

1. **Clone or download the code** into a Colab notebook.
2. **Install dependencies**:

    ```bash
    !pip install google-generativeai pymongo python-dotenv scikit-learn pillow ipywidgets
    ```

3. **Set environment variables** inside the notebook:

    ```python
    os.environ["GEMINI_API_KEY"] = "your_gemini_api_key"
    os.environ["MONGO_URI"] = "your_mongo_connection_uri"
    ```

4. **Run the chatbot** using the provided `run_bot_ui()` function.

---

## 📂 MongoDB Schema (products)

Each product document should include fields like:

```json
{
  "name": "Classic Blue Jeans",
  "description": "High-rise stretch denim with a tapered fit.",
  "category": "bottom",
  "type": "jeans",
  "color": "blue",
  "material": "denim",
  "images": ["https://example.com/image1.jpg"]
}
