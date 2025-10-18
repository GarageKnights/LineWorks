# Underground Electrical Service Estimator

A Progressive Web App (PWA) for estimating underground electrical service installations with materials, labor, and voltage drop calculations.

**Version:** 7.8 GPS/PWA  
**Live App:** https://YOUR_USERNAME.github.io/ug-estimator/

## Features

- **Offline Support** - Works without internet connection
- **Installable** - Add to home screen on iOS, Android, and desktop
- **GPS Integration** - Auto-populate service address from location
- **Voltage Drop Calculation** - Auto-size main conductor based on VD
- **Revenue Credit** - Calculate utility incentives based on heating type
- **Primary/Secondary Lines** - Optional primary and secondary service configurations
- **Photo Capture** - Take and include photos in estimates
- **Print/PDF Export** - Generate shareable PDF estimates
- **Data Persistence** - Save estimates and pricing locally on device
- **CSV Pricing Import** - Update pricing from external CSV file

## Getting Started

### Access the App

1. Go to: `https://YOUR_USERNAME.github.io/ug-estimator/`
2. On mobile: Safari (iOS) or Chrome (Android)
3. Desktop: Any modern browser

### Install as App

**iOS (Safari):**
1. Open Safari
2. Visit the app URL
3. Tap Share button (box with arrow)
4. Select "Add to Home Screen"
5. Confirm

**Android (Chrome):**
1. Open Chrome
2. Visit the app URL
3. Tap Menu (3 dots)
4. Select "Install app"
5. Confirm

**Desktop:**
1. Open in Chrome/Edge
2. Look for install icon in address bar
3. Click and confirm

## Using the Estimator

### Basic Workflow

1. **Enter Job Details**
   - Customer/Job name
   - Service address (or use GPS button)

2. **Set Service Parameters**
   - Service amps (200, 320, or 600)
   - Voltage (240 or 480)
   - Diversified load in amps

3. **Select Installation Method**
   - Direct Bury
   - Direct Bury w/ Conduit
   - Bore

4. **Configure Service Line**
   - Trench length (ft)
   - Asphalt/concrete crossings
   - Number of sweeps and LB fittings

5. **Optional: Primary/Secondary**
   - Check "Primary Required" for utility line work
   - Check "Secondary Required" for additional circuits
   - Configure each separately

6. **Optional: Revenue Credit**
   - Check "Apply Revenue Credit"
   - Select heating type
   - Enter home square footage

7. **Click "Estimate"**
   - App calculates materials and labor
   - Shows itemized breakdown
   - Displays voltage drop analysis

### Key Settings

**Voltage Drop (VD) Check:**
- Auto-sizes main conductor to stay ≤3% VD
- Shows actual VD percentage
- Enforces 3% limit if enabled

**Install Method:**
- **Direct Bury:** No conduit, trenched service
- **Direct Bury w/ Conduit:** PVC/HDPE in trench
- **Bore:** Boring (subcontract costs included)

**Pricing:**
- Edit prices directly in form
- Or import from CSV file (see below)
- All prices saved to device

## Updating Pricing

### Option 1: Manual Edit
1. Expand "Edit Prices & Import"
2. Modify individual prices
3. Changes auto-save

### Option 2: Import from CSV

1. Create a CSV file with format:
```
key,value
materials.conduit_2_in_per_ft,2.60
materials.conduit_3_in_per_ft,3.10
labor.rate_per_hour,85
```

2. Upload CSV to GitHub or any HTTPS server

3. In app:
   - Expand "Edit Prices & Import"
   - Paste CSV URL
   - Click "Update Pricing from CSV"
   - Prices save automatically

**Available Keys:**
- `materials.conduit_*_in_per_ft` (2, 3, 4 inch sizes)
- `materials.hdpe_*_in_per_ft`
- `materials.wire_al_*_per_ft` (2, 1_0, 4_0, 350, 500)
- `labor.rate_per_hour`
- `labor.trenching_ft_per_hour`
- `labor.backfill_ft_per_hour`
- `labor.conduit_install_ft_per_hour`
- `labor.wire_pull_ft_per_hour`
- `labor.terminate_hours`
- And many more accessories and pricing options

## Saving & Loading Data

**Save Current Inputs:**
1. Fill out estimate
2. Click "Save Inputs"
3. Saved to device

**Load Previous Inputs:**
1. Click "Load Inputs"
2. Previous values restore

**Export as JSON:**
1. Click "Save As"
2. Downloads JSON file with all inputs and pricing
3. Can share with team

## Printing & PDF

1. Complete your estimate
2. Click "Share/Print PDF"
3. On iOS: Share menu, Save to Files or Mail
4. On Android: Save to device
5. On Desktop: Print dialog

**PDF includes:**
- Job details and address
- Materials and labor costs
- Itemized breakdown
- Photos (each on own page)

## Offline Use

This app works completely offline:
- First load caches the app
- All calculations happen locally
- Data saved to device storage
- No internet required for estimating

**Note:** GPS and CSV import need internet to function, but core estimating works offline.

## Tips & Tricks

- **Quick Preset:** Use "Quick 200A / 100 ft" button for fast 200A estimates
- **Check Voltage Drop:** Enable "Check VD" to auto-size conductor
- **Photos:** Take photos on-site and include in PDF export
- **Mobile Friendly:** Works great on iPad and mobile devices
- **No Signup Required:** No accounts, no login needed

## Troubleshooting

**App Not Updating After Upload:**
- Clear browser cache (Ctrl+Shift+Delete)
- Try in incognito/private mode
- Wait 5+ minutes for GitHub Pages to refresh

**GPS Not Working:**
- Make sure browser has location permission
- Try turning location on/off
- Use on HTTPS (GitHub Pages is HTTPS)

**CSV Import Fails:**
- Verify URL is HTTPS (not HTTP)
- Check CSV format (comma or semicolon separated)
- Verify column names match exactly

**Data Lost:**
- Data persists in localStorage
- Clearing browser data will erase saved estimates
- Always export important estimates as JSON

## Notes

- **Planning Tool Only** - This is not a formal engineering estimate. Always verify with proper design calculations.
- **No Cloud Backup** - Data stored locally only. Export important estimates.
- **Mobile First** - Designed for iPad/mobile field work but works on desktop.
- **Offline First** - All data stays on device. No tracking or analytics.

## Support

For issues or feature requests, open an issue on GitHub or contact support.

---

**Last Updated:** v7.8  
**License:** MIT