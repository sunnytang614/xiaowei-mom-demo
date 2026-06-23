# Faster Autoplay Design

## Goal

Shorten the 13-page relationship-memory playback from 65.5 seconds to 43.3 seconds without changing content, layout, navigation, or visual transitions.

## Timing strategy

- Title and short transition pages: 2.5–3 seconds.
- Data and narrative pages: 3.2–3.5 seconds.
- Dense chat and comparison pages: 4.5 seconds.
- Final action page: 4 seconds, preserving time to choose an action.

## Acceptance criteria

- The 13 durations are: `2000, 3000, 2000, 4500, 3200, 2800, 2800, 4500, 4500, 3500, 3500, 3000, 4000`.
- Total autoplay duration is 43.3 seconds.
- Existing autoplay, skip, progress, layout, and content behavior remain unchanged.
