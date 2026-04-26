# Psychiatry Department Portal

A modern web-based management portal for the Psychiatry Department with scheduling, staff management, and Google Sheets integration.

## Features

- **Authentication System**: Secure login for staff members
- **Dashboard**: Personalized dashboard with weekly schedule view
- **Schedule Management**: Upload and manage Excel-based staff schedules
- **Google Sheets Integration**: Sync staff data from Google Sheets
- **Staff Directory**: Complete team member directory with search
- **Admin Panel**: Administrative controls for data management

## Quick Start

### Local Development

1. Clone or download this repository
2. Open the project folder
3. Run `python -m http.server 8000` or `npm start`
4. Open `http://localhost:8000` in your browser

### Netlify Deployment

#### Option 1: Drag & Drop (Easiest)
1. Go to [netlify.com](https://netlify.com)
2. Sign up/login
3. Drag the entire project folder onto the deployment area
4. Your site will be live instantly!

#### Option 2: Git Integration
1. Push your code to GitHub/GitLab/Bitbucket
2. Connect your repository to Netlify
3. Netlify will automatically deploy your site

## Default Login Credentials

| Role | Username | Password |
|------|----------|----------|
| Head of Department | hod@psych | hod123 |
| Team A Leader | leaderA | leadA |
| Team B Leader | leaderB | leadB |
| Team C Leader | leaderC | leadC |
| Team D Leader | leaderD | leadD |
| Staff Member | resident1 | member |
| Nurse | nurse1 | nurse |

## Excel Upload Instructions

1. Go to Admin tab (requires admin login)
2. Upload your DOP SCH.xlsx file in the Excel Schedule Upload section
3. The system will automatically parse all sheets and extract schedule data
4. Check the browser console (F12) for detailed parsing information

## Google Sheets Setup

1. Create a Google Sheet with columns: Name, Role, Team, Email
2. Share the sheet publicly (Anyone with link can view)
3. Copy the Sheet ID from the URL (between `/d/` and `/edit`)
4. In Admin tab, paste the Sheet ID and click "Test Connection"
5. If successful, click "Sync from Google Sheets"

## File Structure

```
department/
  psych department.html    # Main application
  netlify.toml            # Netlify configuration
  package.json            # Project metadata
  README.md               # This file
```

## Browser Compatibility

- Chrome/Chromium 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## Security Notes

- All data is stored locally in browser localStorage
- No server-side processing required
- Google Sheets must be shared publicly for integration
- Excel files are processed client-side only

## Troubleshooting

### Excel Upload Issues
- Open browser console (F12) to see detailed parsing logs
- Ensure your Excel file has date headers and staff names
- The system processes ALL sheets automatically

### Google Sheets Issues
- Verify the sheet is shared publicly
- Check that the Sheet ID is correct (no extra characters)
- Ensure your sheet has the required headers: Name, Role, Team, Email

### Performance
- The application works entirely in the browser
- No server costs or maintenance required
- Fast loading with optimized assets

## Support

For technical issues, check the browser console for error messages and ensure all files are properly uploaded to Netlify.
