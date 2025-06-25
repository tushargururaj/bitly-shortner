# Bitly URL Shortener

**Author:** tushargururaj  
**Version:** 0.0.1  
**Type:** Dify Plugin Tool

## Description
This tool allows users to shorten long URLs using the Bitly API and retrieve click analytics for existing Bitly links. When a user provides a standard URL, the tool generates a shortened version that is easier to share and track. If the user inputs an already shortened Bitly link, the tool returns key analytics such as total clicks and geographic distribution, helping users monitor engagement.

## Features
- **Shorten URLs**: Convert long URLs to shortened Bitly links
- **Custom Domains**: Support for custom domains (default: bit.ly)
- **Group Organization**: Associate links with Bitly groups
- **Link Titles**: Add descriptive titles to shortened links
- **Click Analytics**: Retrieve total click counts and engagement data
- **Geographic Distribution**: View click analytics by country
- **Time-based Analytics**: Get analytics for different time periods

## Installation
1. Clone this repository or copy the plugin folder into your Dify plugins directory.
2. Set up a Python virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

## Configuration
1. Get your Bitly access token from the [Bitly Developer Console](https://app.bitly.com/settings/api/)
2. Add your access token in the provider settings in Dify

## Usage Examples

### Shorten a URL
- Provide a long URL to shorten
- Optionally specify custom domain, group GUID, and title
- Returns the shortened Bitly link with metadata

### Get Analytics
- Provide a Bitly link (e.g., bit.ly/abc123)
- Optionally specify time unit and number of units
- Returns total clicks and geographic distribution

## API Endpoints Used
- `POST /v4/shorten` - Shorten URLs
- `GET /v4/bitlinks/{bitlink}/clicks/summary` - Get click summary
- `GET /v4/bitlinks/{bitlink}/countries` - Get geographic distribution
- `GET /v4/user` - Validate access token

## Troubleshooting
- Ensure your Bitly access token is valid and has appropriate permissions
- Check that the Bitly link format is correct (e.g., bit.ly/abc123)
- Verify your Bitly account has the necessary features enabled

## License
MIT



