# CertiVerify

A standalone, universal viewer and verifier for blockcerts credentials. This tool allows users to easily view, share, and verify digital certificates.

## Features
- **Verify Blockcerts**: Automatically verifies Blockcerts records to ensure authenticity.
- **Multiple Display Modes**: View certificates in card, full, or fullscreen mode.
- **Download & Share**: Download records as PDFs or share them on social networks.
- **Customizable**: Tweak themes, locale, and API configurations to suit your needs.

## Quick Start

### 1. Installation
Install the component using npm:
```bash
npm i @blockcerts/blockcerts-verifier
```

### 2. Basic Usage
Import the verifier script and add the `<blockcerts-verifier>` tag to your HTML:

```html
<!-- Load Web Components Polyfill (Required for some browsers) -->
<script src="node_modules/@webcomponents/webcomponentsjs/webcomponents-loader.js"></script>

<!-- Load CertiVerify -->
<script type="module" src="node_modules/@blockcerts/blockcerts-verifier/dist/main.js"></script>

<!-- Add the Verifier Component -->
<blockcerts-verifier src="path/to/certificate.json"></blockcerts-verifier>
```

## Options & Attributes

You can customize the component by adding attributes directly to the `<blockcerts-verifier>` tag:

| Attribute | Description | Example |
|---|---|---|
| `src` | URL or stringified JSON of the certificate to load. | `src="cert.json"` |
| `display-mode` | `card`, `full`, or `fullscreen`. | `display-mode="full"` |
| `theme` | `bright` or `dark`. | `theme="dark"` |
| `locale` | Set language (e.g., `en`, `fr`, `es`). | `locale="fr"` |
| `allow-download` | Allow users to download the record. | `allow-download` |
| `allow-social-share`| Allow sharing on LinkedIn, Facebook, Twitter. | `allow-social-share` |
| `disable-verify` | Disables verification entirely. | `disable-verify` |

*For more advanced API options and configurations, please see the [Demo Pages](/demo).*

## Development & Deployment

### Local Development
```bash
npm install
npm run start
```
*This will open the demo page at `http://localhost:8081/demo/`.*

### Vercel Deployment
This repository is configured for 1-click deployment on Vercel. 
Simply link this repository to your Vercel account, and it will automatically build and deploy.

## License
MIT License
