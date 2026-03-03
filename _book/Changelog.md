# Changelog

  For the complete changelog, see [CHANGELOG.md](https://github.com/HAYASAKA7/HAYA-TAB/blob/main/CHANGELOG.md) in the repository.   

  ## Latest Release

  ### [2.2.12] - 2026-03-02
  - **Fixed:** Initial letter sorting issue where title initials weren't recalculated when metadata was updated
  - **Improved:** Manual metadata updates and MusicBrainz worker now correctly recalculate initials
  - **Improved:** Consistent sorting in Quick Jump Bar across all metadata update paths

  ### [2.2.11] - 2026-02-28
  - **Changed:** Updated wails.json with Windows executable version information
  - **Improved:** Windows builds now display proper version details in file properties

  ### [2.2.10] - 2026-02-28
  - **Added:** Enhanced context menu for tab cards with category operations
  - **Added:** "Add to Category" and "Remove from Category" options
  - **Improved:** Backend protection prevents removal from cloud storage category

  ### [2.2.9] - 2026-02-28
  - **Changed:** Database package refactor - split monolithic database.go into focused modules
  - **Improved:** Better code organization with database_tabs.go, database_categories.go, database_settings.go
  - **Fixed:** Removed trailing whitespace in FTS5 trigger definitions

  ### [2.2.8] - 2026-02-28
  - **Added:** XSS prevention with safeHtml utility function for user-controlled data
  - **Improved:** Dialog messages with user-provided data are now properly escaped
  - **Improved:** Encryption security - replaced hardcoded key with machine-specific PBKDF2-derived key

  ### [2.2.7] - 2026-02-28
  - **Fixed:** Unified toast styling for consistent appearance across all notification types
  - **Improved:** Toast boxes now size based on content with better visual consistency
  - **Improved:** Added hover effect for better user interaction feedback

  ### [2.2.6] - 2026-02-28
  - **Added:** WebDAV improvements with enhanced settings integration
  - **Added:** Updated translations for WebDAV features
  - **Improved:** Better error handling in cloud file operations
  - **Improved:** Settings persistence for WebDAV credentials

  ### [2.2.5] - 2026-02-28
  - **Added:** Customizable data path for storage directory
  - **Added:** Automatic data migration when changing paths

  ### [2.2.0] - 2026-02-27
  - **Added:** A-Z Quick Jump Bar for alphabet navigation
  - **Added:** MusicBrainz integration for artist origin lookup
  - **Added:** Multi-language title sorting (Chinese Pinyin, Japanese Gojūon/Romaji)
  - **Improved:** Cloud category protection

  ### [2.1.0] - 2026-02-26
  - **Added:** MusicXML support (.xml, .musicxml, .mxl)
  - **Improved:** In-place tab operations without page refresh
  - **Fixed:** Scroll position preservation

  ### [2.0.0] - 2026-02-26
  - **Added:** WebDAV integration for cloud storage sync
  - **Added:** Online viewer for cloud files
  - **Added:** Cloud library browser
  - **Improved:** Large file handling performance

  [View Full Changelog →](https://github.com/HAYASAKA7/HAYA-TAB/blob/main/CHANGELOG.md)

  ---