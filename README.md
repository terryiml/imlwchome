# Beecroft → Town Hall transit planner

A small, responsive Traditional Chinese website for checking public-transport journeys from Beecroft Station to Town Hall Station using Transport for NSW Trip Planner data.

## Run locally

Open `index.html` in a modern browser, or serve this directory with any static web server. The page makes requests directly to the TfNSW API.

## Enable live trip data

1. Register for a key through the [Transport for NSW Open Data portal](https://opendata.transport.nsw.gov.au/).
2. Open the site and choose **設定 API 金鑰**.
3. Paste your API key and save, then search for a route.

The key is stored in this browser's `localStorage` only. This static demo calls the API from the browser; if your API subscription or browser environment does not permit direct cross-origin requests, route API calls through a server-side proxy and keep the key there instead of exposing it in client-side code.

The app queries the TfNSW Trip Planner endpoint (`/v1/tp/plan`) for current departures and displays returned journey times, transport legs, and estimated departure information when available. Timetable estimates can change; confirm service details with Transport for NSW before travelling.
