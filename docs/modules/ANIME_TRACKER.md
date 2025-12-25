# Anime Index & Tracker Module

Owner: Sreehari M  
Week: 1 (Documentation Only)  
Scope: Anime/Manga Index + Personal Tracker

---

## 1. Module Overview

This module is responsible for:
- Displaying a list of anime/manga/light novels
- Showing detailed information for each title
- Allowing users to track their watching status
- Storing and retrieving tracker data from Firestore

This module does **not** handle:
- Authentication
- Community posts
- Recommendations logic (only provides data used by it)

---

## 2. Anime Data Structure

Each anime/manga entry is stored as a document in Firestore.

### Collection: `anime`

**Document Fields:**

| Field Name     | Type        | Description |
|---------------|-------------|-------------|
| title         | String      | Anime/Manga title |
| synopsis      | String      | Short description |
| genres        | Array<String> | Genres (Action, Romance, etc.) |
| imageUrl      | String      | Poster / cover image |
| type          | String      | anime / manga / light_novel |
| platforms     | Array<String> | Legal platforms (Netflix, Crunchyroll, etc.) |
| releaseYear   | Number      | Year of release |
| createdAt     | Timestamp   | Added date |

---

## 3. Screens Involved

### 3.1 Explore Screen
- Shows list of anime/manga
- Genre filter
- Search by title
- Clicking an item opens Detail Screen

### 3.2 Anime Detail Screen
- Title, image, synopsis
- Genres
- Where to Watch (platform list)
- Tracker status buttons

### 3.3 Tracker Screen
- Displays user’s tracked items grouped by status:
  - Watching
  - Completed
  - On-Hold

---

## 4. Tracker System

### Tracker Statuses (Fixed)

| Status     | Meaning |
|-----------|---------|
| watching  | Currently watching/reading |
| completed | Finished |
| on_hold   | Paused or stopped |

(No dropped status in MVP to keep scope small.)

---

## 5. Tracker Data Structure

### Collection: `tracker`

Tracker data is stored **per user**, not inside anime documents.

**Structure:**


### Fields:
| Field | Type | Description |
|-----|------|-------------|
| status | String | watching / completed / on_hold |
| updatedAt | Timestamp | Last status change |

---

## 6. Tracker Flow

1. User opens Anime Detail Screen
2. User taps a status button (Watching / Completed / On-Hold)
3. App writes status to:
4. Tracker Screen fetches all anime IDs under the user
5. App fetches anime details using those IDs
6. Items are grouped by status in UI

---

## 7. Firestore Collections Summary

| Collection | Purpose |
|----------|---------|
| anime | Stores anime/manga data |
| tracker | Stores user tracking status |

---

## 8. Notes & Constraints

- Anime data will be **manually added** for MVP
- No external APIs in Week 1
- No streaming or video content
- All platforms listed are legal only
- Simple queries preferred (no joins)

---

## 9. Future Enhancements (Post-MVP)

- Dropped status
- Episode count tracking
- Progress tracking (e.g., episode 5/12)
- Sorting by last updated
- API-based anime data import

---

## 10. Week 1 Status

✅ Data structures defined  
✅ Screens identified  
✅ Firestore collections planned  
❌ No coding done (as per rules)

Ready for Week 2 implementation.
