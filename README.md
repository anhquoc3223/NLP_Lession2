# Text Analysis Web Application

A comprehensive web application for text analysis using Natural Language Processing (NLP) techniques. This application demonstrates the classic NLP pipeline: **Tokenization → POS Tagging → Named Entity Recognition**.

## 🚀 Features

- **Tokenization**: Break text into individual tokens (words, punctuation, etc.)
- **Part-of-Speech (POS) Tagging**: Identify grammatical categories of each token
- **Named Entity Recognition (NER)**: Extract and classify named entities (people, organizations, locations, etc.)
- **Interactive Visualizations**: Charts and graphs for better understanding
- **Color-coded Entity Highlighting**: Visual representation of different entity types
- **Comprehensive Statistics**: Detailed analysis summary with metrics

## 🛠️ Technologies Used

- **spaCy**: Advanced NLP library for tokenization, POS tagging, and NER
- **Streamlit**: Modern web framework for creating interactive data applications
- **Pandas**: Data manipulation and analysis
- **Plotly**: Interactive visualizations and charts

## 📋 Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

## 🔧 Installation

1. **Clone or download this project**
   ```bash
   cd /path/to/your/project
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download spaCy English model**
   ```bash
   python -m spacy download en_core_web_sm
   ```

## 🚀 Running the Application

1. **Start the Streamlit application**
   ```bash
   streamlit run app.py
   ```

2. **Open your web browser**
   - The application will automatically open at `http://localhost:8501`
   - If it doesn't open automatically, manually navigate to the URL shown in the terminal

## 📖 How to Use

### 1. Input Text
- **Option A**: Type your own text in the text area on the left sidebar
- **Option B**: Select one of the provided sample texts from the dropdown menu

### 2. Analyze Text
- Click the **"🔍 Analyze Text"** button to process your input

### 3. View Results
The application provides four main tabs:

#### 🔤 Tokens Tab
- Displays all individual tokens extracted from the text
- Shows token properties (whitespace, alphabetic, digit, punctuation)
- Provides token statistics (total tokens, words, numbers, punctuation)

#### 🏷️ POS Tags Tab
- Shows Part-of-Speech tags for each token
- Displays both coarse-grained and fine-grained POS tags
- Includes lemmatization (root form of words)
- Shows POS tag distribution chart

#### 👥 Named Entities Tab
- Lists all named entities found in the text
- Categorizes entities by type (PERSON, ORG, GPE, etc.)
- Provides entity type distribution pie chart
- **Highlights entities in the original text with different colors**

#### 📊 Summary Tab
- Overall text statistics (characters, words, sentences)
- Entity summary metrics
- Most frequent words chart
- Average word length and other insights

## 🎨 Entity Color Coding

The application uses different colors to highlight various entity types:

- **PERSON** (People): Red
- **ORG** (Organizations): Teal
- **GPE** (Geopolitical entities): Blue
- **LOC** (Locations): Green
- **DATE**: Yellow
- **TIME**: Plum
- **MONEY**: Mint
- **PERCENT**: Light Yellow
- And many more...

## 📊 Sample Texts

The application includes three sample texts to get you started:

1. **News Article**: About Apple Inc. and Tim Cook
2. **Scientific Text**: About research from MIT
3. **Business Report**: About Microsoft's earnings

## 🔍 Understanding the Results

### Tokenization
- **Token**: Individual units of text (words, punctuation, spaces)
- **Whitespace**: Whether the token is followed by whitespace
- **Is Alpha**: Whether the token contains only alphabetic characters
- **Is Digit**: Whether the token contains only digits
- **Is Punctuation**: Whether the token is punctuation

### POS Tagging
- **POS Tag**: Coarse-grained grammatical category (NOUN, VERB, ADJ, etc.)
- **Fine-grained Tag**: More specific grammatical information
- **Lemma**: Root form of the word (e.g., "running" → "run")
- **Stop Word**: Common words that are often filtered out (the, a, an, etc.)

### Named Entity Recognition
- **PERSON**: Names of people
- **ORG**: Organizations, companies, institutions
- **GPE**: Countries, cities, states (geopolitical entities)
- **LOC**: Non-geopolitical locations (mountains, bodies of water)
- **DATE**: Absolute or relative dates
- **TIME**: Times smaller than a day
- **MONEY**: Monetary values
- **PERCENT**: Percentages
- **CARDINAL**: Numerals that don't fall into other categories
- **ORDINAL**: "first", "second", etc.

## 🐛 Troubleshooting

### Common Issues

1. **"spaCy English model not found" error**
   ```bash
   python -m spacy download en_core_web_sm
   ```

2. **Module not found errors**
   ```bash
   pip install -r requirements.txt
   ```

3. **Port already in use**
   - Streamlit will automatically find an available port
   - Or specify a different port: `streamlit run app.py --server.port 8502`

## 📁 Project Structure

```
lesson_2/
├── app.py              # Main Streamlit application
├── requirements.txt    # Python dependencies
└── README.md          # This file
```

## 🎯 Learning Objectives

This application demonstrates:

1. **Text Preprocessing**: How to clean and prepare text for analysis
2. **Tokenization**: Breaking text into meaningful units
3. **Linguistic Analysis**: Understanding grammatical structure
4. **Information Extraction**: Identifying key entities in text
5. **Data Visualization**: Presenting NLP results effectively
6. **Web Application Development**: Creating interactive NLP tools

## 🔮 Future Enhancements

Potential improvements you could add:

- Support for multiple languages
- Sentiment analysis
- Text summarization
- Dependency parsing visualization
- Custom entity recognition
- Export results to CSV/JSON
- Batch processing of multiple texts

## 📚 Additional Resources

- [spaCy Documentation](https://spacy.io/usage)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Natural Language Processing with Python](https://www.nltk.org/book/)

## 🤝 Contributing

Feel free to fork this project and add your own features or improvements!

---

**Happy Text Analyzing! 📝✨**
