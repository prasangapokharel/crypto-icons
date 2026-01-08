# Crypto Icons Collection

A comprehensive collection of cryptocurrency, currency, and UI icons. Access thousands of crypto and currency icons via jsDelivr CDN.

## 🌐 CDN Usage

Use icons directly from our CDN without any installation:

### Crypto Icons (SVG)
```html
<!-- Bitcoin icon -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/btc.svg" alt="Bitcoin">

<!-- Ethereum icon -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/eth.svg" alt="Ethereum">

<!-- Solana icon -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/sol.svg" alt="Solana">
```

### Currency Icons (SVG)
```html
<!-- US Dollar -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/currency/usd.svg" alt="USD">

<!-- Euro -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/currency/eur.svg" alt="EUR">

<!-- British Pound -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/currency/gbp.svg" alt="GBP">
```

### Binance Logos (PNG)
```html
<!-- Bitcoin logo (note: uppercase symbol) -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/binance/BTC.png" alt="Bitcoin">

<!-- Ethereum logo -->
<img src="https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/binance/ETH.png" alt="Ethereum">
```

### In CSS
```css
.crypto-icon {
  background-image: url('https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/btc.svg');
  width: 32px;
  height: 32px;
  background-size: cover;
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

### React Example
```jsx
function CryptoIcon({ symbol }) {
  return (
    <img 
      src={`https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/${symbol}.svg`}
      alt={symbol}
      width="32"
      height="32"
    />
  );
}

// Usage: <CryptoIcon symbol="btc" />
```

## 📊 Available Icons

- **500+ Crypto Icons**: BTC, ETH, SOL, ADA, XRP, DOGE, BNB, and more
- **50+ Currency Icons**: USD, EUR, GBP, JPY, CNY, and more
- **800+ Binance Logos**: High-quality PNG logos for all traded coins

## 🔗 CDN URL Patterns

| Icon Type | URL Pattern | Example |
|-----------|-------------|---------|
| Crypto (SVG) | `https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/crypto/{symbol}.svg` | `btc.svg` |
| Currency (SVG) | `https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/currency/{code}.svg` | `usd.svg` |
| Binance (PNG) | `https://cdn.jsdelivr.net/gh/prasangapokharel/crypto-icons@v1.0.0/binance/{SYMBOL}.png` | `BTC.png` |

**Note:** 
- Use `@v1.0.0` for specific version (recommended for production)
- Omit version tag for latest (e.g., `/crypto-icons/crypto/btc.svg`)
- Binance logos use **uppercase** symbols (BTC, ETH, etc.)
- Crypto/currency icons use **lowercase** symbols (btc, eth, etc.)

## 📝 License

MIT License - See [LICENSE](LICENSE) file for details.

This is a collection of icons from various sources:
- [Binance Icons](https://github.com/VadimMalykhin/binance-icons)
- [Heroicons](https://github.com/tailwindlabs/heroicons) (MIT)
- Binance Logo CDN

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report issues or request new icons
- Submit pull requests
- Improve documentation

## 📮 Support

For issues or questions, please [open an issue](https://github.com/prasangapokharel/crypto-icons/issues) on GitHub.

---

**Version**: 1.0.0  
**Last Updated**: January 2026
