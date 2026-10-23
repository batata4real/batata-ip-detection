# BATATA IP Detection

A small, consent-based web project that displays the public IP address seen by an IP information service, along with approximate location and network-provider details.

## Features

- Public IP lookup using `ipapi.co`
- Approximate city, region, and country display (when provided)
- Network-provider information (when provided)
- Copy-to-clipboard button
- Loading, success, and error messages
- Privacy notice shown before a lookup is started
- Responsive layout and keyboard focus styles
- No dependencies, build tools, or backend required

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a browser.
3. Read the privacy notice and click **I understand — detect my IP**.

Some browsers restrict certain APIs on local files. If needed, run a local static server from the project folder:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Privacy and limitations

- The lookup sends a request to `https://ipapi.co/json/`. That provider receives the connection IP as part of normal web requests and may process it under its own policies.
- This page does not save the IP address to local storage or send it to a server controlled by this project.
- IP-based location is approximate. It is not GPS and cannot reliably identify an exact address.
- A VPN, proxy, mobile carrier, or corporate network may affect the result.
- The page reports the IP seen by the API service. It does not scan other users or intercept WebRTC connections.

## Technologies

- HTML
- CSS
- Vanilla JavaScript
- Fetch API
- Clipboard API (with a fallback)

## Ideas for future improvements

- Add automated tests for formatting and error states.
- Add a clear "data source" section with the provider's current terms and privacy policy.
- Add a manual refresh timestamp.
- Improve localization (English, French, German).

## Author

Add your name or GitHub username here.
