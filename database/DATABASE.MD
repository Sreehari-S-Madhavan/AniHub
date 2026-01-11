# Database

## Overview

The database stores all the data for AniHub, including user information, anime/manga details, and community content.

## Tech Stack

- PostgreSQL

## Structure

- `users`: User accounts and authentication data
- `anime`: Anime titles and metadata
- `manga`: Manga titles and metadata
- `user_tracking`: User's personal lists (watching, completed, etc.)
- `discussions`: Community discussion threads
- `comments`: Comments on discussions

## Setup

1. Install PostgreSQL
2. Create a database named 'anihub'
3. Run the schema scripts to create tables

## Key Tables

- Users table: id, username, email, password_hash
- Anime table: id, title, genre, description
- Tracking table: user_id, content_id, status, progress
