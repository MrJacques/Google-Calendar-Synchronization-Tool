# Google Calendar Synchronization Project - Python Files and Modules

## Core Components

### `main.py`
- **Purpose**: Entry point of the application. Manages command-line arguments, configuration handling, and initiates the synchronization process.
- **Dependencies**: `config`, `calendar_sync`, `utils`.

### `config.py`
- **Purpose**: Handles application configuration, including API credentials, calendar IDs, and user preferences.
- **Dependencies**: Standard libraries (`os`, `json` or `yaml`).

### `calendar_api_client.py`
- **Purpose**: Encapsulates Google Calendar API interactions, including fetching, creating, updating, and deleting events.
- **Dependencies**: `google-api-python-client`, `google-auth`.

### `calendar_sync.py`
- **Purpose**: Contains logic for event comparison, source of truth determination, and event synchronization.
- **Dependencies**: `calendar_api_client`, `utils`.

### `utils.py`
- **Purpose**: Provides utility functions for logging, error handling, and date/time operations.
- **Dependencies**: Standard libraries (`logging`, `datetime`).

## Data Models

### `model/event.py`
- **Purpose**: Defines a data model for calendar events to simplify event data handling.
- **Dependencies**: Standard libraries, possibly `dataclasses`.

## Testing

### `tests/`
- **Purpose**: Houses unit tests for each component of the application.
- **Dependencies**: Testing libraries (`pytest`, `mock`, or `unittest`). Includes tests like `test_calendar_api_client.py`, `test_calendar_sync.py`, and `test_utils.py`.

## Additional Files

- **`requirements.txt`**: Lists project dependencies for easy setup.
- **`Dockerfile`**: Instructions for building the Docker image of the application.
- **`docker-compose.yml`**: Configuration for running the application in Docker containers.
- **`README.md`**: Project overview, setup and usage instructions, and testing info.

This structure ensures a clear separation of concerns, making the application maintainable, scalable, and easy to test.
