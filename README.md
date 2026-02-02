# 🛍️ ThredUp Sales Dashboard

A beautiful, interactive dashboard to visualize your ThredUp closet sales and inventory data. Track revenue, analyze trends, and manage your reselling business with ease.

## ✨ Features

- 📊 **Real-time Analytics** - Track sales, revenue, inventory value, and sell-through rate
- 📈 **Visual Charts** - Sales trends, brand performance, and price distributions  
- 🔄 **Auto-Sync Bookmarklets** - One-click data updates (no file management!)
- 🎯 **Smart Filtering** - Filter by brand, price range, and date
- 💾 **Data Persistence** - Your data is saved automatically in browser storage
- 📱 **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- 🎨 **Beautiful UI** - Modern, clean interface with gradient backgrounds

## 🚀 Quick Start

### 1. Access Your Dashboard

Your dashboard is live at: `https://YOUR-USERNAME.github.io/threadup-dashboard/`

### 2. Set Up Auto-Sync Bookmarklets (Recommended - 2 minutes)

The easiest way to update your dashboard is with **auto-sync bookmarklets**:

See **[AUTO_SYNC.md](./AUTO_SYNC.md)** for complete instructions and bookmarklet code.

**Quick summary:**
1. Create 2 bookmarks in your browser
2. Paste the bookmarklet code as the URL
3. Visit ThredUp → Click bookmarklet → Data syncs instantly!
4. Refresh dashboard → See your data!

### 3. Alternative: Manual Upload (Fallback)

If you prefer manual file uploads or need a backup method, you can still upload JSON files directly to the dashboard. This option is available in the collapsible "Manual Upload" section.

## 📊 Dashboard Components

### Summary Banner
- **Total Business Value** - Combined revenue + inventory value
- **Total Items** - Complete item count (sold + available)
- **Sell-Through Rate** - Percentage of inventory sold

### Statistics Cards (5 Cards)
- **Items Sold** - Number of items sold
- **Revenue (Sold)** - Total $ earned from sales
- **Items Available** - Current inventory count
- **Inventory Value** - Total $ value of available items
- **Avg Sold Price** - Average revenue per item

### Interactive Charts
- **Sales Over Time** - Line chart showing monthly revenue trends
- **Top Brands by Revenue** - Bar chart of your best-performing brands
- **Price Distribution** - Doughnut chart showing price ranges
- **Inventory Status** - Pie chart of sold vs available items

### Data Table
- Searchable, sortable table of all items
- Filter by status (Sold/Available)
- View brand, description, price, and date

## 🔄 Recommended Workflow

### Weekly Update (30 seconds)
```
1. Visit ThredUp Sold page → Scroll → Click bookmarklet
2. Visit ThredUp Available page → Scroll → Click bookmarklet  
3. Refresh dashboard → See updated data!
```

No files to download or upload - just one click per page!

### First-Time Setup
See **[AUTOMATION_GUIDE.md](./AUTOMATION_GUIDE.md)** for complete setup instructions.

## 🛠️ Customization

### Change Colors

Edit the CSS gradients in `index.html`:

```css
body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### Add More Stats

Add new stat cards in the `updateStats()` function:

```javascript
const newStat = `
    <div class="stat-card">
        <div class="stat-label">Your Label</div>
        <div class="stat-value">${yourValue}</div>
    </div>
`;
```

### Create Custom Charts

Use Chart.js to add more visualizations:

```javascript
new Chart(ctx, {
    type: 'bar', // or 'line', 'pie', 'radar', etc.
    data: { ... },
    options: { ... }
});
```

## 📱 Mobile Support

The dashboard is fully responsive and works great on mobile devices. Upload data from your computer and check stats on your phone!

## 🔒 Privacy

- All data is stored locally in your browser (localStorage)
- No data is sent to external servers
- Your ThredUp credentials are never accessed
- Bookmarklets only read public page content

## 🤝 Contributing

Want to improve the dashboard? Here are some ideas:

- [ ] Add export to PDF/Excel functionality
- [ ] Implement advanced filtering options
- [ ] Add profit margin calculator
- [ ] Create seasonal trend analysis
- [ ] Add email notification for sales

## 📝 Data Format

### Sold Items JSON
```json
[
  {
    "Brand": "Nike",
    "Description": "Running Shoes Size 9",
    "Sold Price": 45.00,
    "Date Sold": "January 15, 2026"
  }
]
```

### Available Items JSON
```json
[
  {
    "Brand": "Adidas",
    "Description": "Track Jacket Medium",
    "Price": 35.00,
    "Date Listed": "February 1, 2026"
  }
]
```

## 🐛 Troubleshooting

**Dashboard not loading?**
- Check browser console (F12) for errors
- Ensure you're using a modern browser (Chrome, Firefox, Safari, Edge)
- Clear browser cache and reload

**Data not showing after using bookmarklet?**
- Click the "🔄 Refresh Dashboard" button or press F5
- Make sure you're using the same browser where you ran the bookmarklet
- Check localStorage: F12 → Application → Local Storage → look for threadup_sold/threadup_available

**Bookmarklet not working?**
- Make sure you've scrolled to load all items on ThredUp first
- Check that you copied the entire bookmarklet code
- Try refreshing the ThredUp page and running again

**Data disappeared after closing browser?**
- Check if you're in Private/Incognito mode (disables localStorage)
- Use normal browsing mode for data persistence

## 📚 Technologies Used

- **Chart.js** - Beautiful, responsive charts
- **Vanilla JavaScript** - No framework bloat
- **CSS Grid & Flexbox** - Modern, responsive layouts
- **localStorage API** - Client-side data persistence

## 📄 License

MIT License - Feel free to use and modify for your own purposes!

## 💡 Tips for Success

1. **Regular Updates** - Run bookmarklets weekly to track trends
2. **Backup Data** - Use the export function monthly
3. **Analyze Trends** - Check which brands/price ranges sell best
4. **Optimize Pricing** - Use average price data to set competitive prices
5. **Track Seasonality** - Notice patterns in sales over time

## 🎯 Future Enhancements

- Integration with Google Sheets
- Automated email reports
- Predictive analytics for pricing
- Comparison with ThredUp market averages
- Mobile app version

---

**Questions or suggestions?** Open an issue or submit a pull request!

Happy reselling! 🎉
