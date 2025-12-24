# AniHub — Product Definition

## Overview
AniHub is an anime companion platform designed to help users discover, track, and discuss anime, manga, and light novels in one place.

AniHub is NOT a streaming platform.
It does not host or distribute copyrighted content.
The platform focuses on discovery, organization, community interaction, and guidance toward legal viewing platforms.

## Problem Statement
Anime fans currently use multiple apps and websites to:
- Track what they are watching or reading
- Discover new anime or manga
- Find legal platforms to watch content
- Share opinions, reviews, and debates

AniHub solves this by combining these needs into a single, simple companion app.

## Target Users
- College students
- Beginner anime/manga/light novel fans
- Community-driven anime enthusiasts

## Core Goals (MVP)
- Simple and usable
- Beginner-friendly implementation
- Real-world deployable
- No piracy
- Minimal to no AI usage

## MVP Features (Locked Scope)

### 1. User Authentication & Profile
- Email/password login
- Basic profile:
  - Username
  - Avatar
  - Favorite genres

### 2. Anime / Manga Index
- List of anime with:
  - Title
  - Synopsis
  - Genres
  - Image
- Search by title
- Filter by genre

### 3. Personal Tracker
- Users can track anime as:
  - Watching
  - Completed
  - On-Hold
- Tracker stored per user

### 4. Rule-Based Recommendations
- Based on:
  - User favorite genres
  - Previously tracked anime
- No machine learning or AI

### 5. Where to Watch (Legal)
- Show legal platforms (Netflix, Crunchyroll, etc.)
- External links only

### 6. Community Feed
- Text and image posts
- Anime-related content only
- No private messaging

### 7. Structured Debate System
- Posts support:
  - Agree
  - Disagree
- Simple vote counting
- No comments in MVP

## Non-Goals (Out of Scope)
- Video streaming
- Pirated content
- AI-based recommendations
- Real-time chat
- Notifications
- Follow system
- Admin/moderation tools

## Tech Stack
- Frontend: Flutter
- Backend: Firebase (Auth, Firestore, Storage)

## Success Criteria
- User can sign up, explore anime, track progress, and participate in community debates
- App runs without crashes
- Clear structure for future expansion
