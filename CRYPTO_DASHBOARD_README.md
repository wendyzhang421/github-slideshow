# 🚀 Crypto Price Dashboard

A modern, real-time cryptocurrency price dashboard featuring Bitcoin and Ethereum with live price tracking, charts, and market data.

## Features

- **Real-time Prices**: Live Bitcoin and Ethereum prices updated every 30 seconds
- **Price Charts**: Interactive price trend visualization using Chart.js
- **Market Data**: 24-hour price changes, market cap, and trading volume
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern UI**: Beautiful glassmorphism design with smooth animations
- **Error Handling**: Graceful error handling with retry functionality

## How to Use

### Method 1: Direct File Access
Simply open `crypto-dashboard.html` in your web browser.

### Method 2: Local Server (Recommended)
For the best experience and to avoid CORS issues:

1. Start a local server:
   ```bash
   python3 -m http.server 8000
   ```

2. Open your browser and go to:
   ```
   http://localhost:8000/crypto-dashboard.html
   ```

## Technical Details

### Data Source
- **API**: CoinGecko API (free, no authentication required)
- **Update Frequency**: Every 30 seconds
- **Data Points**: Price, 24h change, market cap, trading volume

### Technologies Used
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Charts**: Chart.js library
- **Styling**: CSS Grid, Flexbox, CSS animations
- **API**: Fetch API for HTTP requests

### Browser Support
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Dashboard Components

### Price Cards
Each cryptocurrency displays:
- Current USD price
- 24-hour percentage change (green for positive, red for negative)
- Market capitalization
- 24-hour trading volume
- Cryptocurrency icon and symbol

### Price Chart
- Real-time line chart showing price trends
- Dual Y-axis for Bitcoin and Ethereum (different price scales)
- Rolling 20-point history
- Responsive chart that adapts to screen size

### Status Indicators
- Loading spinner during data fetch
- Last updated timestamp
- Error messages with retry option
- Connection status indicators

## Customization

To add more cryptocurrencies, modify the `cryptos` array in the JavaScript:

```javascript
this.cryptos = ['bitcoin', 'ethereum', 'cardano', 'polkadot'];
```

And add corresponding entries in the `cryptoInfo` object with proper names, symbols, and icon URLs.

## API Rate Limits

The CoinGecko free API allows:
- 10-30 calls per minute
- No authentication required
- Current configuration is well within limits

## Troubleshooting

### Dashboard Not Loading
- Check internet connection
- Ensure JavaScript is enabled
- Try refreshing the page
- Check browser console for errors

### Outdated Prices
- Verify internet connection
- CoinGecko API may be experiencing issues
- Try the retry button

### Chart Not Displaying
- Ensure Chart.js CDN is accessible
- Check for JavaScript errors in console
- Try clearing browser cache

## License

This project is open source and available under the MIT License.