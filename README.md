# 🎬 Smartsage — Movie Information Extractor

Smartsage is an AI-powered movie information extractor that converts an unstructured movie description into structured data.

Simply paste a movie paragraph, and the application uses an LLM to identify important movie details such as the title, release year, genre, director, cast, rating, and summary.

## ✨ Features

* 🎬 Extract movie title
* 📅 Extract release year
* 🎭 Identify movie genres
* 🎥 Extract director
* 👥 Extract cast members
* ⭐ Extract movie rating
* 📝 Generate a concise summary
* 🤖 Uses AI/LLM for information extraction
* 📦 Returns structured data using a Pydantic schema
* 🌐 Streamlit-based web interface

## 🛠️ Tech Stack

* **Python**
* **Streamlit** — Web UI
* **LangChain** — LLM application framework
* **Mistral AI** — Language model
* **Pydantic** — Structured output validation
* **python-dotenv** — Environment variable management

## 📂 Project Structure

```text
smartsage/
│
├── core.py
├── uicore.py
├── requirements.txt
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/anikettsuri/smartsage.git
cd smartsage
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## 🔑 Environment Variables

Create a `.env` file in the project directory:

```env
MISTRAL_API_KEY=your_mistral_api_key
```

Never commit your API key or `.env` file to GitHub.

## ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run uicore.py
```

The application will open in your browser.

## 🧪 Example Input

```text
Inception is a 2010 science fiction thriller film directed by Christopher Nolan and starring Leonardo DiCaprio, Joseph Gordon-Levitt, Ellen Page, Tom Hardy, and Ken Watanabe. The story follows Dom Cobb, a skilled thief who enters people's dreams to steal valuable secrets. Cobb is given a chance to erase his criminal past if he can successfully perform an unusual task called inception, which involves planting an idea inside someone's mind. The film explores dreams, reality, memory, and human emotions. Inception received widespread critical acclaim and has an IMDb rating of around 8.8 out of 10.
```

## 📤 Example Output

```json
{
  "title": "Inception",
  "release_year": 2010,
  "genre": [
    "Science Fiction",
    "Thriller"
  ],
  "director": "Christopher Nolan",
  "cast": [
    "Leonardo DiCaprio",
    "Joseph Gordon-Levitt",
    "Ellen Page",
    "Tom Hardy",
    "Ken Watanabe"
  ],
  "rating": 8.8,
  "summary": "A skilled thief enters people's dreams to steal secrets and is tasked with planting an idea inside someone's mind."
}
```

## 🧠 How It Works

```text
Movie Description
       ↓
   Streamlit UI
       ↓
     LangChain
       ↓
    Mistral LLM
       ↓
Structured Output
       ↓
   Pydantic Validation
       ↓
Movie Information
```

The user provides a natural-language movie description. The application sends the text to the LLM with instructions to extract predefined movie fields. The response is then validated against a Pydantic model to ensure the extracted information follows the expected structure.

## 🚀 Deployment

The application can be deployed using Streamlit Community Cloud.

Set the following secret in the deployment environment:

```text
MISTRAL_API_KEY
```

Then use:

```text
Repository: anikettsuri/smartsage
Branch: main
Main file: uicore.py
```

## 🔮 Future Improvements

* Support for multiple LLM providers
* Movie poster generation
* IMDb/TMDB API integration
* Confidence scores for extracted information
* Batch movie extraction
* Export results as JSON/CSV
* Improved handling of missing information
* Movie recommendation functionality

## 👨‍💻 Author

**Aniket Suri**

GitHub: https://github.com/anikettsuri

## 📄 License

This project is intended for educational and portfolio purposes.
