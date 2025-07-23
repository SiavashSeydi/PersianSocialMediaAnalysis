# Persian Telegram Topic Modeling

This project scrapes Persian-language Telegram channels (e.g., Iran International) and applies natural language processing to extract and visualize war-related topics using BERTopic.

## Features

- Scrapes thousands of Telegram messages using Telethon
- Persian text cleaning, normalization, and tokenization
- Phrase modeling (bigrams) using Gensim
- Topic modeling using BERTopic and Sentence-Transformer embeddings

## Technologies Used

- Python, Telethon, Pandas, Hazm, Gensim
- BERTopic, UMAP, HDBSCAN
- Sentence-Transformers (`xmanii/maux-gte-persian`)

---

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/PersianSocialMediaAnalysis.git
cd PersianSocialMediaAnalysis
```

### 2. Create and activate a Conda environment

```bash
conda create -n persian_media python=3.10
conda activate persian_media
conda install --file requirements.txt
```

### 3. Configure your environment

Create a `.env` file based on the template:

```bash
copy .env.example .env   # On Windows
# OR
cp .env.example .env     # On macOS/Linux
```

Edit `.env` and add your Telegram API ID and hash:

```env
TG_API_ID=your_api_id
TG_API_HASH=your_api_hash
```

## Future Work
- Improving the tokenization and topic extraction
- Integrate interactive topic exploration (e.g., Streamlit or PyLDAvis)
- Support scraping multiple channels in parallel

---

## Acknowledgments

- [Hazm](https://github.com/sobhe/hazm) for Persian NLP tools  
- [BERTopic](https://github.com/MaartenGr/BERTopic) for flexible topic modeling  
- [Xmanii](https://huggingface.co/xmanii/maux-gte-persian) for Persian embeddings
