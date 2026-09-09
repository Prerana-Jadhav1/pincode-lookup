# Pincode Lookup

A React app to look up Indian Postal Pincode details using the Postal Pincode API, with real-time filtering, a loader, and error handling.

## Overview

- **Lookup form** — User enters a 6-digit pincode and clicks "Lookup" to fetch data from `https://api.postalpincode.in/pincode/<PINCODE>`.
- **Results display** — Shows Post Office Name, Pincode, District, and State for each post office returned.
- **Filter** — A separate input filters the displayed results by post office name in real time (no loader needed for filtering).
- **Loader** — A custom CSS spinner is shown while the API call is in progress, and hidden once data is fetched.
- **Error handling**:
  - Non-6-digit input shows "Please enter a valid 6-digit pincode" without calling the API.
  - Failed/invalid API responses show the API's error message or a generic failure message.
  - If filtering results in an empty list, shows "Couldn't find the postal data you're looking for..."

## Tech Stack

- React 16
- Webpack 4 (dev server + production build)
- Fetch API

## Project Structure

```
src/
  components/
    App.js       # Form, fetch logic, filter, loader, results rendering
  styles/App.css  # Styling incl. loader animation
  index.js
  index.html
```

## Scripts

```bash
npm install     # install dependencies
npm start        # run dev server (webpack-dev-server)
npm run build     # production build
```

## Key Features

- `useState` used for pincode input, filter text, post office list, loading state, error state, and searched flag
- Fetch triggered only on valid 6-digit pincode
- Real-time filtering without re-fetching
- Custom CSS loader shown only during the API call
- Clear error and empty-state messaging
