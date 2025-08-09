# Crypto Signals Dashboard

## Overview

This is an enhanced cryptocurrency dashboard that displays comprehensive market indicators and trends with live charting capabilities. The application features a spectacular introduction page showcasing "The Greatest of All Time: Nuno Vieira Gonçalves" with premium UI design, followed by a professional dashboard showing real-time crypto market data including total market capitalization, Bitcoin dominance, Fear & Greed index, Altcoin Season Index, and worldwide Bitcoin search trends. Features include interactive charts with 1-year historical data, status indicators, smooth navigation between intro and dashboard pages, and modern glass-morphism design with animated elements.

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
- **Spectacular Introduction Page** - Premium landing page celebrating "The Greatest of All Time: Nuno Vieira Gonçalves" with animated background blobs, crown icon, and professional typography
- **Smooth Page Navigation** - Seamless transitions between introduction and dashboard with "Enter Dashboard" and "Back to Intro" buttons
- **Modern Glass-Morphism UI** - Enhanced design with backdrop blur effects, gradient backgrounds, hover animations, and professional card layouts
- **Status Indicators** - Color-coded badges for Fear & Greed Index (Extreme Fear/Fear/Neutral/Greed/Extreme Greed) and Altcoin Season Index (BTC Season/Mixed Market/ALT Season)
- **Altcoin Season Index** - Calculated indicator based on Bitcoin dominance to estimate altcoin market phase
- **Historical Data Charts** - Four interactive charts displaying 365 days (1 year) of historical trends with moving averages
- **Moving Average Smoothing** - Charts use 14-day and 21-day moving averages to reduce variance and show cleaner trends
- **Enhanced Error Handling** - Improved API retry logic and loading states to prevent "API Error" messages

### Browser APIs
- **Fetch API** - For making HTTP requests to external services
- **DOM API** - For updating page content dynamically
- **Intl API** - For currency and date formatting