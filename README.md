![Metrics](/github-metrics.svg)

## Mealie v3.4.0

This repository includes a Docker Compose configuration for deploying [Mealie](https://github.com/mealie-recipes/mealie) v3.4.0, a self-hosted recipe manager and meal planner.

### Quick Start

1. Clone this repository:
```bash
git clone https://github.com/slamp/slamp.git
cd slamp
```

2. Start Mealie:
```bash
docker-compose up -d
```

3. Access Mealie at http://localhost:9000

### Configuration

The `docker-compose.yml` file includes:
- **Image**: `ghcr.io/mealie-recipes/mealie:v3.4.0`
- **Port**: 9000 (customizable)
- **Database**: SQLite (default)
- **Storage**: Named volume `mealie-data`

### Features in v3.4.0

- Per-device default activity settings (recipes, shopping lists, or meal planner)
- Improved shopping list label sections
- Various bug fixes and maintenance updates

For more information, see the [official release notes](https://github.com/mealie-recipes/mealie/releases/tag/v3.4.0).
