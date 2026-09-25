# 🏆 Le Chaudron : LoL Ranked Dashboard

🔗 **Live Demo:** https://dejavu-sandbox.github.io/lol-dashboard/

A sleek League of Legends ranked statistics dashboard built with vanilla HTML/CSS/JavaScript and powered by Azure Functions.

## 📋 Features

- **Real-time Player Stats** - Displays current rank, LP, and win rates for tracked players
- **Match History** - View detailed match information including champions, kills/deaths/assists, and game duration
- **Daily LP Tracking** - 24-hour LP changes and trend indicators
- **Responsive Design** - Dark LoL-themed interface with smooth animations
- **Interactive Modals** - Click on players to expand detailed match history
- **Auto-refresh** - Updates data every 60 seconds (configurable)

## 🚀 Quick Start

1. **Open the dashboard:**
   - Hosted on GitHub Pages or your preferred host
   - No build process needed - pure HTML/CSS/JavaScript

2. **Configuration:**
   Update the API endpoint in the JavaScript:
   ```javascript
   const apiUrl = "https://your-azure-function-app.azurewebsites.net/api/GetLoLStats";
   ```

3. **Access:**
   - Dashboard auto-loads player stats on page load
   - Manual refresh: Reload the page or wait for auto-refresh (60s)

## 🎮 Tracked Players

The following League of Legends summoners are tracked:

- **Gourdin Puissant** (Tag: CHIER)
- **Megumin Full AP** (Tag: EUW)
- **BlasterFly** (Tag: EUW)
- **Green Goober** (Tag: GOOB)
- **Macon Capule** (Tag: CHIER)

## 📊 UI Components

### Main Table
- **Rank** - Current rank with division and LP
- **Win Rate** - Calculated from recent matches
- **Kills/Deaths/Assists** - Average stats from last 20 matches
- **Daily LP** - Change in LP over the last 24 hours

### Match Details (Modal)
- **Champion** - Champion played in the match
- **Result** - Win/Loss indicator
- **K/D/A** - Individual match statistics
- **Duration** - Game length
- **Date** - When the match was played

## 🔧 Technical Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Backend:** Azure Functions (PowerShell)
- **API:** Riot Games League of Legends API
- **Hosting:** GitHub Pages (frontend), Azure Functions (backend)

## 🔐 Security & CORS

- **Auth Level:** Anonymous (configured in Azure Portal)
- **CORS Allowed Origins:**
  - Azure Portal
  - GitHub Pages deployment URL

**Note:** The Riot API key is stored securely in Azure Function App Settings.

## 📱 Browser Support

- Chrome/Edge (Latest)
- Firefox (Latest)
- Safari (Latest)
- Mobile browsers (responsive design)

## 📝 Notes

- Refresh interval: 60 seconds (prevents API rate limiting)
- Daily LP snapshot captured at 00:05 UTC
- Last 20 matches are displayed per player
- Win rate calculated from visible match history

## 🔗 Related Projects

- **Backend API:** [lol-dashboard-backend](https://github.com/dejavu-sandbox/lol-dashboard-backend)
  - Azure Functions powering this dashboard
  - Handles Riot API calls and daily snapshots

## 📚 Documentation

- [Riot Developer Portal](https://developer.riotgames.com)
- [League of Legends API Documentation](https://developer.riotgames.com/apis)
- [Azure Functions Documentation](https://learn.microsoft.com/en-us/azure/azure-functions/)

## 📄 License

MIT License - Feel free to use, modify, and redistribute this project as you wish.