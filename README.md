# PlayNow Platform Rewriter

A Chrome extension that automatically modifies API requests to Play Now — a Polish streaming service provided by Play. The extension sets the `platform` parameter to `APPLE_TV` to enable additional features.

## Installation

### English

1. Clone or download this repository
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode" in the top right corner
4. Click "Load unpacked" and select the directory containing the extension files
5. The extension should now be installed and active

### Polski

1. Sklonuj lub pobierz to repozytorium
2. Otwórz Chrome i przejdź do `chrome://extensions/`
3. Włącz "Tryb programisty" w prawym górnym rogu
4. Kliknij "Załaduj rozpakowane" i wybierz katalog zawierający pliki rozszerzenia
5. Rozszerzenie powinno być teraz zainstalowane i aktywne

### Using the CRX file (Alternative Installation)

#### English

1. Download the latest CRX file from the [Releases](https://github.com/bibixx/play-now/releases) page
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode" in the top right corner
4. Drag and drop the downloaded CRX file onto the extensions page
5. Confirm the installation when prompted

#### Polski

1. Pobierz najnowszy plik CRX ze strony [Releases](https://github.com/bibixx/play-now/releases)
2. Otwórz Chrome i przejdź do `chrome://extensions/`
3. Włącz "Tryb programisty" w prawym górnym rogu
4. Przeciągnij i upuść pobrany plik CRX na stronę rozszerzeń
5. Potwierdź instalację po wyświetleniu monitu

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
