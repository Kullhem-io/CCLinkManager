# CC Link Manager

A modern web application for managing and joining Zoom calls, built with Astro and deployed on GitHub Pages.

## Features

- **Complete Call History**: View both upcoming and past Zoom calls
- **Individual Join Buttons**: Each call has its own join button for easy access
- **Troubleshooting Friendly**: See all calls (upcoming and past) to help diagnose issues
- **Real-time Updates**: Automatically updates when new calls are added
- **Modern UI**: Clean, responsive design with tabbed interface
- **Copy Links**: Copy Zoom links to clipboard with one click
- **Time Remaining**: Shows countdown for upcoming calls

## Technology Stack

- **Astro**: Modern static site generator for optimal performance
- **Firebase Firestore**: Real-time database for call information
- **GitHub Pages**: Free hosting and deployment
- **Vanilla JavaScript**: No framework dependencies for maximum compatibility

## Setup

1. **Install Dependencies** (if Node.js is available):
   ```bash
   npm install
   ```

2. **Development Server**:
   ```bash
   npm run dev
   ```

3. **Build for Production**:
   ```bash
   npm run build
   ```

## Deployment

This project is configured for automatic deployment to GitHub Pages:

1. Push changes to the `main` branch
2. GitHub Actions will automatically build and deploy the site
3. The site will be available at: `https://yourusername.github.io/CCLinkManager`

## Configuration

Update the following files for your specific setup:

- `astro.config.mjs`: Update the `site` URL with your GitHub username
- `src/pages/index.astro`: Update Firebase configuration if needed

## Database Structure

The Firebase Firestore collection `calls` should contain documents with:

```javascript
{
  url: "https://zoom.us/j/123456789",
  subject: "Weekly Team Meeting",
  start: firebase.firestore.Timestamp.fromDate(new Date("2024-01-15T14:00:00Z"))
}
```

## Browser Support

Works in all modern browsers that support:
- ES6+ JavaScript
- CSS Grid and Flexbox
- Fetch API
- Clipboard API (for copy functionality)
