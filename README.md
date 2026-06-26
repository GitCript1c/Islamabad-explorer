# Islamabad Viewpoints Explorer

Islamabad Viewpoints Explorer is a single-file, browser-based map app for discovering scenic viewpoints in Islamabad, Pakistan. It combines a Leaflet map, viewpoint cards, filters, geolocation, theme switching, and a simple route planner into one self-contained HTML file.

## Features

- Interactive Leaflet map centered on Islamabad
- Viewpoint cards with ratings, amenities, and highlights
- Filterable viewpoints, including places with restaurants
- Route planner between viewpoints
- Geolocation support to find the nearest viewpoint
- Light and dark theme toggle with saved preference
- Toast notifications and polished responsive UI

## How It Works

All structure, styling, data, and behavior live in [islamabad-explorer.html](islamabad-explorer.html). The page loads its dependencies from CDNs, including:

- Leaflet for maps
- Font Awesome for icons
- Google Fonts for typography

The route feature uses an in-memory graph and straight-line distance calculations between viewpoints. It is intended for exploration and demonstration, not turn-by-turn road navigation.

## Getting Started

1. Clone the repository:

	```bash
	git clone https://github.com/GitCript1c/Islamabad-explorer.git
	```

2. Open the project folder in VS Code or your editor of choice.

3. Run the page from a local web server or localhost. For example, with Python:

	```bash
	python -m http.server 8000
	```

4. Open the app in your browser:

	```text
	http://localhost:8000/islamabad-explorer.html
	```

## Notes

- The app expects browser features like geolocation to work best on localhost or another local server, not `file://`.
- Theme preference is stored in `localStorage` under `islamabad-theme`.
- The app is designed as a single-file project, so changes to HTML, CSS, and JavaScript usually need to be coordinated together.

## Project Structure

- [islamabad-explorer.html](islamabad-explorer.html) - the entire application
- [AGENTS.md](AGENTS.md) - workspace guidance for agents
- [LICENSE](LICENSE) - repository license

## License

See [LICENSE](LICENSE) for details.
