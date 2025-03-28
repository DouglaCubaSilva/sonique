# Sonique

## Overview
Sonique is a music streaming platform that allows users to listen to their favorite songs, create playlists, and explore new music. Inspired by Spotify, Sonique introduces a unique feature: the **Mix Service**, which enables users to remix tracks, merge multiple songs, cut parts, and modify audio channels like a DJ.

## Requirements
- Open-source and free technologies to minimize costs.
- Implementation of SonarQube for code quality analysis.
- Dependency-Check for security assessment of third-party libraries.
- Structured Git workflow ensuring controlled development and rollback capabilities.
- Microservices architecture for scalability and maintainability.

## Architecture
Sonique is built with a microservices-based architecture, ensuring modularity and scalability. The core services include:
- **User Service**: Manages authentication, profiles, and user preferences.
- **Music Service**: Handles the music catalog, metadata, and streaming.
- **Mix Service**: Allows remixing of tracks, merging, cutting, and modifying audio channels.
- **Playlist Service**: Manages user-generated playlists and music recommendations.
- **Search Service**: Provides fast and efficient music search and filtering.
- **BFF (Backend for Frontend)**: Acts as an API gateway, optimizing communication between microservices and the frontend.

## Microservices
Each microservice operates independently and communicates via APIs. The key microservices are:
1. **User Service**: Handles authentication, authorization, and user settings.
2. **Music Service**: Manages metadata, storage, and streaming of music files.
3. **Mix Service**: Provides tools for audio remixing, merging, and manipulation.
4. **Playlist Service**: Enables users to create, manage, and share playlists.
5. **Search Service**: Implements full-text search, filtering, and tagging.
6. **BFF**: Serves as an API gateway for frontend interactions.

This documentation will be continuously updated as the project evolves.

