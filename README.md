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

### Security Considerations

**Important**: The default configuration is designed for easy setup but includes some settings that should be adjusted for production:

1. **ALLOW_SIGNUP**: Set to `"true"` by default to allow initial account creation. After creating your admin account, set this to `"false"` to prevent unauthorized signups.
2. **RECIPE_PUBLIC**: Set to `"true"` by default, making recipes publicly accessible. Set to `"false"` if you want private recipe collections.
3. **Expose to Internet**: If exposing Mealie to the internet, consider using a reverse proxy with HTTPS (like Nginx or Traefik) and proper authentication.

### Features in v3.4.0

- Per-device default activity settings (recipes, shopping lists, or meal planner)
- Improved shopping list label sections
- Various bug fixes and maintenance updates

For more information, see the [official release notes](https://github.com/mealie-recipes/mealie/releases/tag/v3.4.0).
