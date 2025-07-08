# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a simple HTML-based plate labeler application for laboratory microplates (6, 12, 24, 48, 96, or 384 wells). The application is entirely self-contained in a single HTML file (`platelabeler.html`) using React with Babel for transpilation.

## Architecture

- **Single-file application**: All code is contained in `platelabeler.html`
- **React components**: Uses React 18 via CDN with Babel standalone for JSX transpilation
- **Styling**: Tailwind CSS via CDN with custom print styles
- **State management**: React hooks for local component state
- **No build process**: Runs directly in the browser

## Key Components & Logic

- `PlateLabeler`: Main React component managing all application state
- `PLATE_MAP`: Configuration object defining plate dimensions for different well counts
- Label system supports three types: row labels, column labels, and cell-specific labels
- Empty well marking system with special print handling for visibility
- Interactive painting modes: eraser and empty well marking
- Print optimization with grayscale filter for empty wells

## Development

To work with this application:
- Open `platelabeler.html` directly in a web browser
- No build, compile, or server setup required
- All dependencies loaded via CDN
- For testing, use browser developer tools

## Key State Variables

- `plate`: Current plate size (6-384 wells)
- `labels`: Object storing all well labels by position key
- `selecting`: Boolean for multi-well selection mode
- `eraser`/`emptyMode`: Tool modes for well manipulation
- `edgeEmpty`: Toggle for marking edge wells as empty

The application uses a grid-based coordinate system with string keys formatted as "row-col" for tracking well positions and their associated labels.