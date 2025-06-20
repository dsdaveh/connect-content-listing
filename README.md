# Content Listing Dashboard

A Quarto-based dashboard that displays a clean, organized listing of publicly accessible content from a Posit Connect server. The dashboard presents content in an easy-to-navigate grid layout with direct links to each item.

## Features

- multi-column grid layout that adapts to different screen sizes
- Direct links to content items
- Secure handling of API credentials
- Automatic content filtering for public access items
- Customizable through CSS styling

## Prerequisites

- R (version 4.0.0 or higher)
- Required R packages:
  - dplyr
  - stringr
  - connectapi
  - DT

## Setup

1. Install required R packages:
```r
install.packages(c("dplyr", "stringr", "connectapi", "DT"))
```

2. Create a `.Renviron` file in your home directory with the following variables:
```
CONNECT_SERVER_URL=your-connect-server-url
CONNECT_API_KEY=your-api-key
```

Replace:
- `your-connect-server-url` with your Posit Connect server URL (e.g., "https://connect.example.com/")
- `your-api-key` with your Posit Connect API key

## Usage

1. Ensure your `.Renviron` file is properly configured
2. Open `content-listing.qmd` in RStudio
3. Click "Render" to generate the dashboard

The dashboard will automatically:
- Connect to your Posit Connect server
- Retrieve all publicly accessible content
- Display items in a responsive grid layout
- Provide direct links to each content item

## Security Notes

- Never commit your `.Renviron` file to version control
- Keep your API key secure and rotate it periodically
- The dashboard only displays publicly accessible content

## Customization

The dashboard's appearance can be customized by modifying the CSS styles in the Quarto document. The current styling includes:
- Responsive grid layout
- Hover effects
- Clean typography
- Mobile-friendly design 
