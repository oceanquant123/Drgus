# Chinese Herbal Medicine Market Price Scraper

This project is a high-performance web scraper designed to collect market price data from **[Zhongyao Cai Tian Di Wang](https://www.zyctd.com/)** (Chinese Herbal Medicine Market Network), a leading platform for traditional Chinese medicine pricing information in China.

Built with a **multi-process + thread pool** concurrency architecture, the scraper efficiently handles large-scale data extraction while maintaining robustness and scalability.

---

## 🚀 Features

- **High Concurrency**: Leverages multiprocessing combined with multithreading to maximize throughput and minimize latency.
- **Robust Error Handling**: Automatically retries failed requests and gracefully handles network issues or unexpected page structures.
- **Structured Data Output**: Exports scraped data in clean, structured formats (e.g., CSV, JSON) for easy analysis.
- **Respectful Crawling**: Implements polite crawling practices (rate limiting, user-agent rotation) to comply with website terms and avoid overloading servers.
- **Modular Design**: Easy to extend for scraping additional pages or adapting to site changes.

---

## 🛠️ Tech Stack

- **Language**: Python 3.8+
- **Core Libraries**:
  - `requests` / `httpx` – for HTTP requests
  - `BeautifulSoup4` / `lxml` – for HTML parsing
  - `concurrent.futures` – for thread and process management
  - `logging` – for detailed operation logs
- **Optional Enhancements**:
  - `fake-useragent` – for dynamic user-agent rotation
  - `pandas` – for data export and manipulation

---

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/chinese-herbal-market-scraper.git
   cd chinese-herbal-market-scraper
   ```

2. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   # or
   venv\Scripts\activate     # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## ▶️ Usage

Configure your scraping targets (e.g., herb categories, date ranges) in `config.py` or via command-line arguments.

Run the main script:
```bash
python scraper.py
```

Output files (e.g., `prices_20260320.csv`) will be saved to the `data/` directory by default.

> ⚠️ **Note**: Always check `robots.txt` and terms of service of the target website before scraping. Use responsibly.

---

## 📁 Project Structure

```
├── scraper.py              # Main entry point
├── config.py               # Configuration settings
├── parsers/
│   └── zyctd_parser.py     # HTML parsing logic
├── utils/
│   ├── logger.py           # Logging setup
│   └── helpers.py          # Utility functions
├── data/                   # Output directory (auto-created)
├── requirements.txt        # Dependencies
└── README.md
```

---

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for bug fixes, performance improvements, or new features.

---

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## ⚠️ Disclaimer

This tool is for **educational and research purposes only**. The author does not endorse or encourage unauthorized data harvesting. Always ensure compliance with the target website’s terms of use and applicable laws.
