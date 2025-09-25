# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple meeting cost calculator microsite built as a single HTML file with vanilla JavaScript. The application calculates the real-time cost of meetings based on the number of participants and their hourly rates.

## Architecture

- **Single-file application**: Everything is contained in `index.html`
- **Vanilla JavaScript**: No frameworks or build tools
- **Self-contained**: All CSS and JavaScript are inline
- **Timer-based**: Uses `setInterval()` for real-time updates every second
- **Cost calculation**: Formula is `people × hourly_rate × (elapsed_seconds / 3600)`

## Key Components

- **Timer system**: Tracks elapsed time with play/pause/reset functionality
- **Cost calculator**: Real-time calculation updating every second
- **Input controls**: Number of people and hourly rate per person
- **Display components**: Timer display (HH:MM:SS), cost display, and rate summary

## Development

Since this is a static HTML file, no build process is required. Simply open `index.html` in a web browser to run the application.

The application state is managed through global JavaScript variables:
- `startTime`: When the current timer session began
- `elapsedTime`: Total accumulated time from previous sessions
- `isRunning`: Current timer state
- `timerInterval`: Reference to the setInterval timer

## Testing

Manual testing can be done by:
1. Opening `index.html` in a web browser
2. Verifying timer functionality (start/pause/reset)
3. Checking cost calculations with different people counts and rates
4. Ensuring the display updates correctly every second