# Y.Bookmark

## Overview

Y.Bookmark reimagines bookmark management through the lens of plain text. At its heart lies a single Markdown file - a format that has stood the test of time, offering unparalleled portability and compatibility. While tools like Obsidian have shown the power of local-first file management, Y.Bookmark applies this principle specifically to bookmark organization, creating a sustainable approach to managing your digital references.

## Philosophy

The foundation of Y.Bookmark is built on a simple yet powerful idea: your bookmarks should live in a format that transcends any particular software. By using a single Markdown file as the source of truth, we achieve several key benefits:

1. Universal Compatibility: Whether it's Google Drive, NAS storage, or Git repositories, your bookmarks can be synchronized and backed up using any file management tool you prefer.

2. Local-First: Your data remains under your control, stored as plain text that can be edited with any text editor, while our interface simply makes this interaction more convenient.

3. Future-Proof: Plain text files have existed since the dawn of computing and will continue to be readable long after any particular software ceases to exist.

## Getting Started

When you first launch Y.Bookmark, you'll be prompted to either select an existing bookmark directory or create a new one. The application maintains a minimalist structure:

```plaintext
your-chosen-directory/
├── myBookmark.md     # Your primary bookmark file
├── assets/           # Preview images
└── history/         # Version history
```

## Core Components

The heart of Y.Bookmark is the markdown file format. Each bookmark entry follows this structure:

```markdown
[Title](URL)
tags: [star, work/projects]
![Preview](./assets/image.jpg)

> Description or notes (should have a blank line after)

Something else - will not be displayed

---
```

This format combines readability with flexibility, allowing for rich organization through tags while remaining easy to edit manually when desired.

## Features

### File-First Approach

The application serves as an enhancement layer over your bookmark file, not a replacement for it. You can:

- Edit through the GUI for convenience
- Modify the markdown file directly
- Use the sync button to reconcile changes
- Maintain version history automatically

### Smart Organization

- Tag-based organization using curly braces
- Nested folders using forward slashes (e.g., `work/projects`)
- Support for multiple contexts of the same URL
- Reserved tags like `star` for special features

## Technical Architecture

Built with pywebview, Y.Bookmark provides a native-feeling interface while maintaining its file-centric approach. The application runs quietly in your system tray, monitoring your bookmark file and providing easy access when needed.

### Data Management

All operations center around the markdown file:

- Direct file system monitoring for external changes
- Automatic history preservation
- Asset management for preview images
- Format validation with optional remote assistance

### Edit

We highly recommend using Obsidian to open your myBookmark folder for the best editing experience.

Obsidian's automatic image handling makes it particularly well-suited for managing bookmark preview images.
just remember:

- set the "Attachment folder path" to the `assets` folder in your Obsidian vault settings
- set the "New link format" to `Relative path to file`

## Roadmap

### Phase 1: Core File Management

- [x] Technology selection (pywebview)
- [ ] Markdown-centric implementation
- [ ] File monitoring and sync
- [ ] Basic GUI interface

### Phase 2: System Integration

- [ ] System tray implementation
- [ ] Autostart capability
- [ ] Background operation
- [ ] Cross-platform support

### Phase 3: Enhanced Features

- [ ] Remote format assistance
- [ ] Advanced search capabilities
- [ ] Import tools for common bookmark formats

## Contributing

Y.Bookmark welcomes contributions that align with its file-first philosophy. Whether you're improving the GUI, enhancing markdown parsing, or adding new features, please ensure that the core principle of file-based storage remains central to any changes.

## Licensing

This project is dual-licensed:

1. [GNU Affero General Public License v3.0 (AGPL-3.0)](LICENSE)
2. Commercial License

For commercial use without AGPL-3.0 obligations, please [contact us](mailto:email@alterxyz.org).

## Support

For questions, feature requests, or support:

- Open an issue in the GitHub repository
- Contact us at [email@alterxyz.org](mailto:email@alterxyz.org)

---

This project is currently in alpha. We appreciate your feedback and contributions as we work to improve and expand the system.

**Important**: By contributing to this project, you agree to transfer all rights and ownership of your contributions to the project. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.
