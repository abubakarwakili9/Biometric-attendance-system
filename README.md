# Biometric Attendance System

A modern web-based biometric attendance management system with fingerprint simulation, built with React and deployed on GitHub Pages.

## Features

- 👤 **User Registration**: Enroll users with simulated fingerprint capture
- 🔐 **Attendance Logging**: Track attendance with biometric verification
- 📊 **Dashboard**: Real-time statistics and overview
- 📈 **Reports**: Generate and export attendance reports to CSV
- 💾 **Data Persistence**: All data stored locally in browser (localStorage)
- 📱 **Responsive Design**: Works on desktop, tablet, and mobile devices

## Live Demo

Your deployed system will be available at:
```
https://YOUR_USERNAME.github.io/biometric-attendance-system/
```

## Deployment Guide to GitHub Pages

### Prerequisites
- A GitHub account
- Git installed on your computer (optional, you can use GitHub web interface)

### Method 1: Using GitHub Web Interface (Easiest)

1. **Create a new repository on GitHub:**
   - Go to https://github.com/new
   - Repository name: `biometric-attendance-system`
   - Description: "Biometric Attendance Management System"
   - Make it Public
   - Click "Create repository"

2. **Upload the index.html file:**
   - On your new repository page, click "uploading an existing file"
   - Drag and drop the `index.html` file
   - Commit message: "Initial commit - Add biometric attendance system"
   - Click "Commit changes"

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages (left sidebar)
   - Under "Source", select "Deploy from a branch"
   - Branch: Select `main` (or `master`)
   - Folder: Select `/ (root)`
   - Click "Save"

4. **Wait for deployment (1-2 minutes):**
   - GitHub will build and deploy your site
   - Your site will be live at: `https://YOUR_USERNAME.github.io/biometric-attendance-system/`

### Method 2: Using Git Command Line

1. **Create a new repository on GitHub** (as above)

2. **Initialize and push your project:**
```bash
# Navigate to your project folder
cd /path/to/your/project

# Initialize git repository
git init

# Add the index.html file
git add index.html
git add README.md

# Commit the files
git commit -m "Initial commit - Add biometric attendance system"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/biometric-attendance-system.git

# Push to GitHub
git branch -M main
git push -u origin main
```

3. **Enable GitHub Pages** (same as Method 1, step 3)

### Method 3: Using GitHub Desktop (GUI)

1. **Install GitHub Desktop** from https://desktop.github.com/

2. **Create repository:**
   - File → New Repository
   - Name: `biometric-attendance-system`
   - Local Path: Choose where to save
   - Click "Create Repository"

3. **Add files:**
   - Copy `index.html` to the repository folder
   - GitHub Desktop will detect the new file

4. **Commit and Publish:**
   - Write commit message: "Initial commit"
   - Click "Commit to main"
   - Click "Publish repository"
   - Uncheck "Keep this code private"
   - Click "Publish Repository"

5. **Enable GitHub Pages** (same as Method 1, step 3)

## Usage Guide

### 1. Register Users
- Navigate to "Register User" tab
- Enter user details:
  - Full Name
  - User ID (unique identifier)
  - Department
- Click "Enroll User"
- Wait for simulated fingerprint scan (2 seconds)

### 2. Log Attendance
- Navigate to "Log Attendance" tab
- Click "Scan Fingerprint"
- System randomly selects a registered user (simulates real fingerprint match)
- 94% success rate simulation

### 3. View Dashboard
- See total users enrolled
- Today's attendance count
- System success rate
- List of all registered users

### 4. Generate Reports
- Navigate to "Reports" tab
- Optional: Set date range filters
- View all attendance records
- Export to CSV for external use

## Technical Details

### Technologies Used
- **React 18**: UI framework
- **Tailwind CSS**: Styling via CDN
- **Lucide Icons**: Icon library
- **localStorage**: Data persistence

### Browser Compatibility
- Chrome (recommended)
- Firefox
- Safari
- Edge
- Any modern browser with JavaScript enabled

### Data Storage
All data is stored locally in your browser using localStorage:
- `biometric_users`: User registration data
- `biometric_attendance`: Attendance records

**Note**: Data persists only in the browser where it was created. Clearing browser data will reset the system.

## Customization

### Change Color Scheme
The system uses Tailwind CSS. To customize colors, modify the class names in `index.html`:
- Primary color: `indigo-600` → change to `blue-600`, `purple-600`, etc.
- Success color: `green-600`
- Error color: `red-600`

### Adjust Success Rate
Find line with `Math.random() < 0.94` and change `0.94` to your desired success rate (0.0 to 1.0)

### Modify Scan Duration
Find `setTimeout(..., 2000)` and change `2000` to desired milliseconds

## Security Considerations

⚠️ **Important**: This is a demonstration system with simulated biometric functionality.

For production use, you would need:
- Real biometric hardware integration
- Backend server for secure data storage
- User authentication and authorization
- Encryption for sensitive data
- Audit trails and compliance measures

## Troubleshooting

### Site not loading after deployment
- Wait 2-5 minutes for GitHub Pages to build
- Check Settings → Pages for deployment status
- Ensure the repository is public

### Data not persisting
- Check browser's localStorage settings
- Ensure cookies/storage is enabled
- Try a different browser

### Fingerprint scan not working
- This is a simulation - it should work automatically
- Check browser console (F12) for errors
- Ensure JavaScript is enabled

## Future Enhancements

Potential improvements for the system:
- [ ] Real fingerprint device integration
- [ ] Backend database (Firebase, Supabase, etc.)
- [ ] User authentication
- [ ] Multi-organization support
- [ ] Advanced reporting and analytics
- [ ] Email notifications
- [ ] Mobile app version
- [ ] Photo capture during enrollment
- [ ] Geolocation tracking
- [ ] Shift management

## Support

If you encounter issues:
1. Check the browser console for errors (Press F12)
2. Verify GitHub Pages is enabled in repository settings
3. Ensure all files are properly uploaded
4. Clear browser cache and reload

## License

MIT License - Feel free to use and modify for your projects

## Credits

Developed as a demonstration of modern web technologies for attendance management systems.

---

**Note**: This system uses simulated biometric functionality for demonstration purposes. For production deployment with real biometric devices, additional hardware integration and security measures are required.
