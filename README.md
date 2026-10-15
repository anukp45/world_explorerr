# 🌍 World Quest — Interactive World Explorer

World Quest is an interactive geography application built with Python and Flask. Explore countries, cities, islands, and landmarks on an interactive world map, discover geographical facts, test your knowledge with quizzes, and challenge friends in multiplayer geography duels.

## ✨ Features

- 🗺️ **Interactive World Map** — Explore locations using Leaflet and OpenStreetMap.
- 🌎 **Country Explorer** — Discover capitals, languages, population, area rankings, neighbouring countries, and other geographical facts.
- 🏙️ **City and Settlement Search** — Search populated places using the GeoNames gazetteer.
- 🏝️ **Explore Islands and Landmarks** — Find interesting geographical locations around the world.
- 🔎 **Search and Filters** — Find locations and narrow down your exploration.
- 📚 **Location Details** — View information about selected countries and places.
- 🧠 **Geography Quizzes** — Test your knowledge with quizzes covering different geography themes.
- 🎮 **Solo Mode** — Play geography quizzes on your own.
- 🤝 **Multiplayer Duels** — Challenge another player using a six-character room code.
- 🎨 **Avatar Customization** — Personalize your player profile.
- 📅 **Geography Events** — Explore upcoming geography-related events.
- 📱 **Responsive Design** — Use the application on desktop and mobile screens.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Application logic |
| Flask | Web framework |
| SQLite | Database storage |
| HTML and CSS | Page structure and styling |
| JavaScript | Interactive features |
| Leaflet | Interactive maps |
| OpenStreetMap | Map tiles |
| GeoNames | Populated-place data |
| REST Countries | Country information |
| World Bank | Population data |

## 📁 Project Structure

```text
world_explorer/
├── app.py
├── requirements.txt
├── world_explorer.db
├── README.md
├── data/
│   ├── allCountries.zip
│   ├── countries.json
│   ├── country_facts.json
│   ├── settlements.sqlite
│   ├── rest-countries-source.json
│   ├── world-bank-population-2024.json
│   ├── unesco-source.xml
│   └── national-dishes-wiki.json
├── scripts/
│   ├── build_settlements.py
│   └── enrich_country_facts.py
├── static/
│   ├── css/
│   │   └── styles.css
│   └── js/
│       └── app.js
└── templates/
    └── index.html
```

## 🚀 Getting Started

### Prerequisites

- Python 3.12 or a compatible Python version
- pip
- A modern web browser
- An internet connection for online map tiles and external data services

### 1. Clone the Repository

Replace `YOUR_REPOSITORY_URL` with your GitHub repository URL.

```bash
git clone YOUR_REPOSITORY_URL
cd world_explorer
```

### 2. Create a Virtual Environment

**Windows**

```bash
python -m venv venv
venv\Scripts\activate
```

**macOS/Linux**

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
python app.py
```

### 5. Open World Quest

Visit the following address in your browser:

[http://localhost:5000](http://localhost:5000)

The application initializes its SQLite database when it starts, according to its setup logic.

## 🗃️ Data Sources

World Quest uses several sources to provide geographical information:

- **GeoNames** — Populated-place data, including cities, towns, and villages. GeoNames data is licensed under CC BY 4.0.
- **REST Countries** — Country information.
- **World Bank** — Population figures for 2024.
- **UNESCO listings** — World Heritage-related information.
- **Wikipedia** — Reference information for representative national dishes.
- **CountriesNow** — Country coordinate data used in the country catalog.

Data availability varies by location. Food entries are representative examples, not necessarily official national dishes. Rankings depend on the entries and measurements available in the dataset.

## 🔄 Rebuilding Data Files

The project includes scripts for rebuilding settlement and country-fact datasets.

### Rebuild the Settlement Database

Make sure `data/allCountries.zip` is available, then run:

```bash
python scripts/build_settlements.py
```

This rebuilds the local `data/settlements.sqlite` database.

### Regenerate Country Facts

The enrichment script requires the following source files:

- `data/settlements.sqlite`
- `data/unesco-source.xml`
- `data/national-dishes-wiki.json`
- `data/rest-countries-source.json`
- `data/world-bank-population-2024.json`

Then run:

```bash
python scripts/enrich_country_facts.py
```

Follow the script's output to verify that the generated files were updated successfully.

## 🎮 Multiplayer

World Quest includes a prototype turn-based multiplayer duel system. Players can join a room using a six-character room code, answer geography questions, and compete.

**Note:** The current multiplayer implementation uses SQLite and periodic browser polling. It is a prototype, not a production-ready matchmaking system.

## ⚠️ Data and Project Limitations

- Some locations may have incomplete or unavailable information.
- Rankings reflect the available catalog and may include territories as well as countries.
- Missing measurements are not intended to be guessed.
- Some historical or disputed entries may be identified separately.
- Online map tiles and external services may require an internet connection.
- Multiplayer security and matchmaking would need further work before public production deployment.

## 🔮 Future Improvements

Potential enhancements include:

- More detailed state, province, and regional information.
- Additional landmarks and geographical points of interest.
- More quiz categories and difficulty levels.
- Improved multiplayer matchmaking and real-time communication.
- More comprehensive offline support.
- Expanded accessibility and language options.
- Automated tests and continuous integration.

## 🤝 Contributing

Contributions, bug reports, and feature suggestions are welcome.

1. Fork the repository.
2. Create a branch for your changes.
3. Make and test your changes.
4. Submit a pull request describing your contribution.

## 📄 License

Add the project's chosen license before distributing it publicly. Review the terms of the third-party datasets and services you use, and provide the required attribution.

## 🙌 Acknowledgements

Thanks to the developers and maintainers of Flask, Leaflet, OpenStreetMap, GeoNames, REST Countries, the World Bank, UNESCO data providers, and other sources that support geographical exploration.

---

**Explore the world. Discover new places. Challenge your geography knowledge.**

🌍 Welcome to World Quest!
