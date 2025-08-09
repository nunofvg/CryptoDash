# Crypto Signals Dashboard

## Overview

This is an enhanced cryptocurrency dashboard that displays comprehensive market indicators and trends with live charting capabilities. The application provides real-time data about the crypto market including total market capitalization, Bitcoin dominance, Fear & Greed index, Altcoin Season Index, and worldwide Coinbase app rankings. Features include interactive charts showing data variation over time and direct links to Google Trends analysis. It's designed as a single-page application that aggregates multiple data sources into a clean, responsive interface with Chart.js visualizations.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Single-page application** built with vanilla HTML, CSS, and JavaScript
- **Responsive design** using Tailwind CSS framework loaded via CDN
- **Client-side data fetching** with async/await pattern for API calls
- **Real-time updates** on page load with timestamp display and refresh capability
- **Grid-based layout** that adapts from 1 column on mobile to 5 columns on large screens
- **Interactive charting** using Chart.js library for data visualization

### Data Display Strategy
- **Card-based interface** with individual containers for each metric including new Altcoin Season Index
- **Loading states** showing placeholder text (—) until data loads
- **Error handling** with detailed console logging and fallback displays for failed API requests
- **Live charts** displaying data trends over time with automatic updates
- **Color-coded indicators** for Fear & Greed and Altcoin Season metrics
- **Direct Google Trends links** replacing iframe due to embedding restrictions

### API Integration Pattern
- **Multiple API calls** executed concurrently using Promise-based fetching
- **Data transformation** applied to format currency values and percentages
- **Fallback handling** for missing or invalid data responses

## External Dependencies

### Third-party APIs
- **CoinGecko API** (`api.coingecko.com`) - Provides global cryptocurrency market data including total market cap and Bitcoin dominance percentage
- **Alternative.me Fear & Greed Index** (`api.alternative.me`) - Supplies crypto market sentiment indicator with numerical value and classification
- **Apple RSS API** (`rss.applemarketingtools.com`) - Delivers App Store rankings for finance category apps in US and UK markets (worldwide proxy)
- **Google Trends** (`trends.google.com`) - Direct links to Bitcoin search trend data for Portugal and worldwide analysis

### Frontend Libraries
- **Tailwind CSS** (`cdn.tailwindcss.com`) - Utility-first CSS framework for styling and responsive design
- **Chart.js** (`cdn.jsdelivr.net`) - Interactive charting library for real-time data visualization

### New Features Added
- **Altcoin Season Index** - Calculated indicator based on Bitcoin dominance to estimate altcoin market phase
- **Historical Data Charts** - Four interactive charts displaying 365 days (1 year) of historical trends with moving averages
- **Moving Average Smoothing** - Charts use 14-day and 21-day moving averages to reduce variance and show cleaner trends
- **Data Persistence** - Historical chart data loaded from APIs for comprehensive trend analysis

### Browser APIs
- **Fetch API** - For making HTTP requests to external services
- **DOM API** - For updating page content dynamically
- **Intl API** - For currency and date formatting