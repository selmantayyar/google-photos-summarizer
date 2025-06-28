# Google Photos Summarizer Sample App
This project is designed to query a user's Google Photos library to extract and present a statistical summary, namely the aggregate counts of all photo and video assets.

## Cloud Project Configuration

Ensure that your Google Cloud project is set up following the "Configure your app" guide: [https://developers.google.com/photos/overview/configure-your-app](https://developers.google.com/photos/overview/configure-your-app)
Don't forget to add your google user as test user in "Google Auth Platform / Audience" menu.

## App Setup

With node js and npm installed, run:

> npm install

Then edit config.js with your client id and secret.


## Run in development mode (auto-reload on save)

This will run the app in a development mode that will reload the server whenever you make changes to the application.

> npm run dev

CAUTION: don't check in any changes to config.js (client id or secret). Use a config-test file (or gitignore config.js) instead.


## Running the app

To just run the app (if you're not doing any development), run:

> npm run server

## View metadata summary

After signing in and selecting media items, navigate to `/list` to view a JSON-formatted summary of the count of photos and videos grouped by creation date (per day).

Additionally, the summary is saved to a file in the directory specified by the `jsonSaveLocation` configuration in `config.cjs`. The file is named `DDMMYYYY_DDMMYYYY.json`, with dates in descending order (newest first, oldest second) to avoid confusion.


