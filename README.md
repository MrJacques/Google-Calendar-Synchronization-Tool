
# Google Calendar Synchronization Tool

## Overview

This Python-based tool automates the synchronization of events between two Google Calendar accounts. It ensures that any event created, updated, or deleted in one calendar is mirrored in the other, utilizing a common identifier for events to maintain synchronization and identify their origin. The tool dynamically determines the source of truth based on the latest modification timestamps of events, ensuring the most current event information is always synchronized across both calendars.

## Functional Requirements

1. **Event Synchronization**: Events in both calendars with a matching synchronization ID are kept in sync. Changes include creations, updates, and deletions.
2. **ID Retention**: Custom synchronization IDs are used to link corresponding events across calendars.
3. **Dynamic Source of Truth**: The calendar with the latest event update (based on modification timestamp) dictates the synchronized content.
4. **Error Handling**: Graceful management of API errors, conflicts, and connectivity issues with comprehensive logging.
5. **Unit Testing**: Inclusion of detailed unit tests for core functionalities and error handling scenarios.

## Development Guidelines

### Coding Best Practices

- Adherence to the PEP 8 style guide for Python code.
- Clear variable naming, modular code structure, and detailed commenting.
- Secure handling of sensitive information, such as API keys, using environment variables.

### Documentation

#### README.md

- **Project Description**: An overview of the tool's capabilities and synchronization strategy.
- **Setup Instructions**: Detailed steps for setting up Google API credentials and environmental prerequisites.
- **Usage Guide**: Command-line instructions for initiating synchronization, with examples.
- **Testing Instructions**: Guidelines on running the unit tests to ensure functionality.

#### requirements.txt

- Lists all dependencies required by the tool for easy installation via pip.

#### Docker Support

- **Dockerfile**: Instructions for building a Docker image containing the tool, facilitating easy deployment.
- **docker-compose.yml**: Defines how to run the tool as a Docker container, including configuration for environment variables and volume mounts.

### Testing

- Use of the pytest framework for writing and executing unit tests.
- Mocking of external API calls to ensure tests are self-contained.

### Error Handling

- Comprehensive logging of both operational activities and errors.
- Notification mechanisms for synchronization errors requiring manual intervention.

## Implementation Notes

- Utilization of the Google Calendar API Python Client Library for calendar interactions.
- Consideration of Google API rate limits and implementation of retry strategies.
- Optional database or file-based tracking for event synchronization statuses.

## Docker Integration

### Dockerfile

A Dockerfile is provided to build a Docker image for the tool, ensuring it can run in any environment that supports Docker.

### docker-compose.yml

The docker-compose.yml file simplifies the deployment of the tool as a Docker container, specifying environment configurations and any required services.

## Conclusion

This tool provides a robust solution for synchronizing events between two Google Calendar accounts, leveraging Docker for ease of deployment and operation. By following the guidelines and requirements outlined in this document, developers can ensure a high-quality, maintainable, and efficient synchronization tool.
