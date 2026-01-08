# Crypto Icons Collection

A comprehensive collection of cryptocurrency, currency, and UI icons. Access thousands of crypto and currency icons via jsDelivr CDN or download them for local use.

## 🌐 CDN Usage (jsDelivr)

Use icons directly from our CDN without any installation:

### Crypto Icons (SVG)
```html
<!-- Bitcoin icon -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/btc.svg" alt="Bitcoin">

<!-- Solana icon -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/sol.svg" alt="Solana">

<!-- Use latest version (not recommended for production) -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons/crypto/btc.svg" alt="Bitcoin">
```

### Currency Icons (SVG)
```html
<!-- US Dollar -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/currency/usd.svg" alt="USD">

<!-- Euro -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/currency/eur.svg" alt="EUR">
```

### Binance Logos (PNG)
```html
<!-- Bitcoin logo from Binance -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/binance/BTC.png" alt="Bitcoin">
```

### In CSS
```css
.crypto-icon {
  background-image: url('https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/btc.svg');
  width: 32px;
  height: 32px;
}
```

### In JavaScript
```javascript
// Fetch icon dynamically
const iconUrl = 'https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/btc.svg';
fetch(iconUrl)
  .then(response => response.text())
  .then(svg => document.getElementById('icon').innerHTML = svg);
```

## 📥 Local Development

For contributors and developers who want to maintain the icon collection:

## 📦 What's Included

- **Crypto Icons** - Cryptocurrency icons from Binance Icons repository
- **Currency Icons** - Fiat currency icons 
- **Binance Logos** - Official coin logos from Binance CDN
- **Heroicons** - Tailwind's beautiful hand-crafted SVG icons

## 📂 Directory Structure

```
crypto-icons/
├── crypto/           # Cryptocurrency SVG icons
├── currency/         # Fiat currency SVG icons
├── binance/          # Binance coin logos (PNG)
├── heroicons/        # Heroicons outline 24px SVG icons
├── download.py       # Download crypto icons from GitHub
├── download_currency.py   # Download currency icons
├── download_binance.py    # Download Binance logos via API
└── icons.py          # Download Heroicons
```

## 🚀 Quick Start

### Prerequisites

```bash
pip install aiohttp requests beautifulsoup4
```

### Download All Icons

**1. Download Crypto Icons**
```bash
python download.py
```
Downloads from: `github.com/VadimMalykhin/binance-icons/tree/main/crypto`  
Output: `crypto/`

**2. Download Currency Icons**
```bash
python download_currency.py
```
Downloads from: `github.com/VadimMalykhin/binance-icons/tree/main/currency`  
Output: `currency/`

**3. Download Binance Logos**
```bash
python download_binance.py
```
Downloads from: Binance API + CDN (`bin.bnbstatic.com`)  
Output: `binance/`

**4. Download Heroicons**
```bash
python icons.py
```
Downloads from: `github.com/tailwindlabs/heroicons/tree/master/src/24/outline`  
Output: `heroicons/outline/`

## 🎯 Features

- ✅ **Async/Concurrent Downloads** - Fast downloads with configurable concurrency (30 simultaneous downloads)
- ✅ **Smart Caching** - Skips already downloaded files
- ✅ **Dynamic Symbol Fetching** - Automatically discovers new coins via Binance API
- ✅ **Error Handling** - Gracefully handles missing files and network errors
- ✅ **Clean Progress Output** - Visual feedback for each download
  - ✓ Success
  - ✗ Failed/Not found
  - ⊙ Already exists

## 📖 Usage Examples

### Download Specific Icons

Each script can be run independently:

```bash
# Only get cryptocurrency icons
python download.py

# Only get currency icons  
python download_currency.py

# Only get Binance logos (dynamically fetches all traded coins)
python download_binance.py

# Only get Heroicons
python icons.py
```

### Customization

Edit the configuration section in each script:

```python
# Example: Change concurrency
CONCURRENCY = 50  # Download 50 files at once

# Example: Change output directory
OUT_DIR = Path("my-icons")
```

## 🔄 Keeping Icons Updated

Simply re-run the scripts to fetch new icons:

```bash
python download_binance.py
```

The scripts will automatically:
- Discover new coins/icons
- Skip existing files
- Download only what's missing

## 📊 Statistics

- **Crypto Icons**: ~500+ SVG files
- **Currency Icons**: ~50+ SVG files
- **Binance Logos**: 800+ PNG files (dynamic)
- **Heroicons**: 290+ SVG files

## 🛠️ Technical Details

### Architecture

All download scripts follow the same pattern:
1. Fetch icon list from GitHub API or Binance API
2. Create concurrent download tasks with semaphore limiting
3. Download and save to appropriate directories
4. Provide real-time progress feedback

### Dependencies

- `aiohttp` - Async HTTP client
- `requests` - Sync HTTP client (for Binance API)
- `beautifulsoup4` - HTML parsing (if needed)
- `pathlib` - Cross-platform path handling

## 🔗 CDN Links Reference

| Icon Type | CDN Pattern | Example |
|-----------|-------------|---------|
| Crypto (SVG) | `https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/{symbol}.svg` | `crypto/btc.svg` |
| Currency (SVG) | `https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/currency/{code}.svg` | `currency/usd.svg` |
| Binance (PNG) | `https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/binance/{SYMBOL}.png` | `binance/BTC.png` |
| Heroicons (SVG) | `https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/icons/{name}.svg` | `icons/home.svg` |

**Note:** Use `@v1.0.0` format for specific version. For latest (not recommended in production), omit the version tag.

## 📝 License

MIT License - See [LICENSE](LICENSE) file for details.

This is a collection of icons from various sources. Please refer to the original repositories for their specific licensing:

- [Binance Icons](https://github.com/VadimMalykhin/binance-icons)
- [Heroicons](https://github.com/tailwindlabs/heroicons) (MIT)
- Binance Logo CDN

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Add new icon sources
- Improve download scripts
- Fix bugs
- Update documentation

## 📮 Support

For issues or questions, please open an issue on GitHub.

---

**Version**: 1.0.0  
**Last Updated**: January 2026
