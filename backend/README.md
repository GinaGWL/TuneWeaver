# 🎵 TuneWeaver: Curate Your Unique Sonic Journey 🎧

“Crafting your musical soulmate with personalized, data-driven recommendations.”

TuneWeaver is a modern music discovery application that generates personalized playlists with minimal effort. It analyzes listening preferences and leverages large-scale playlist data to recommend tracks and assemble bespoke playlists that evolve with your taste.

## 📚 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Dataset](#-dataset)
- [Quick Start](#-quick-start)
- [Local Development](#-local-development)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [License](#-license)

## 🚀 Overview

Keeping up with new releases and finding hidden gems is hard. TuneWeaver bridges the gap with a personalized discovery experience. By combining preference modeling with large-scale playlist patterns, it delivers high-quality recommendations and auto-generated playlists tailored to you.

## ✨ Features

- **Personalized suggestions**: Preference-aware track and artist recommendations.
- **Playlist generation**: Build playlists by mood, genre, or seed artists.
- **Trend discovery**: Surface popular tracks across genres.
- **Containerized runtime**: Run locally via Docker in minutes.

## 📂 Dataset

TuneWeaver uses the Spotify Million Playlist Dataset, a large-scale corpus of user playlists for training and evaluation.

- Dataset: [Spotify Million Playlist Dataset](https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge)
- Place `.json` files under `producer/data/` before running the app

Example snippet (abridged):

```json
{
  "name": "musical",
  "pid": 5,
  "num_tracks": 12,
  "tracks": [
    {
      "pos": 0,
      "artist_name": "Degiheugi",
      "track_name": "Finalement",
      "duration_ms": 166264
    }
  ]
}
```

## 🧪 Quick Start

Prerequisites:

- Install Docker: `https://www.docker.com/get-started`

Clone the repository:

```bash
git clone https://github.com/GinaGWL/TuneWeaver.git
cd TuneWeaver
```

Add dataset files:

- Download the full dataset from the link above and place the `.json` files under `producer/data/`.

Build and run:

```bash
docker-compose build
docker-compose up
```

Open the app:

- Navigate to `http://localhost:80` in your browser.

## 🔧 Local Development

- Ensure `producer/data/` contains the dataset `.json` files.
- Use Docker for a consistent environment. If you prefer running services individually, mirror the container configuration locally.

## 🗂 Project Structure

High-level layout (key folders):

- `producer/` — data ingestion/processing and dataset files under `producer/data/`
- `docker-compose.yml` — multi-service orchestration for local runtime
- `proj/` — project documentation and meta files

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request.

1. Fork the repo on GitHub
2. Create a feature branch
3. Commit changes with clear messages
4. Open a pull request with context and screenshots if applicable

## 📄 License

This project is licensed under the MIT License. See `LICENSE` for details.

--—

Maintained by `@GinaGWL` — GitHub: [`https://github.com/GinaGWL`](https://github.com/GinaGWL)
