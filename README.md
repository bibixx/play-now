# PlayNow Platform Rewriter

A Chrome extension that automatically modifies API requests to PlayNow by setting the `platform` parameter to `APPLE_TV`.

## Installation

1. Clone or download this repository
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode" in the top right corner
4. Click "Load unpacked" and select the directory containing the extension files
5. The extension should now be installed and active

## How it works

The extension automatically modifies all requests to `https://playnow.pl/api/*` by:

- Adding `platform=APPLE_TV` if the parameter doesn't exist
- Replacing the existing `platform` parameter with `APPLE_TV` if it exists

## Files

- `manifest.json` - Extension configuration
- `rules.json` - Declarative rules for request modification

## Development

This extension uses Chrome's Manifest V3 and the `declarativeNetRequest` API to modify requests without using a background script.

## License

MIT
