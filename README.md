# Changelog

All notable changes to Cloudy will be documented in this file.

## [V2.0.0Alpha] - Major Backup System Improvements - 2025-05-23

### Added
- **🚀 NEW: Compression-Based Backup System**
  - ZIP compression for Google Drive backups dramatically speeds up uploads
  - Single compressed file upload vs. hundreds/thousands of individual files
  - 20-80% size reduction depending on file types
  - Significantly reduces Google Drive API calls and overhead
  - Timestamp-based archive naming for easy identification

- **⏰ Scheduled Backup System Implementation**
  - Fixed non-functional scheduled backups (e.g., daily 2:30am backups)
  - Added comprehensive scheduling logic for daily, weekly, monthly backups
  - Intelligent scheduling that prevents duplicate runs
  - Proper tracking of last run times

- **🔧 Google Drive Status Unification**
  - Unified Google Drive connection status between Dashboard and Settings
  - Global status manager with intelligent caching (30-second cache)
  - Automatic cache invalidation on authentication changes
  - Consistent status display across the entire application

### Fixed
- **📊 Progress Bar Issues**
  - Fixed progress bar disappearing during backup calculation phase
  - Resolved stuck "starting backup" status while files uploaded in background
  - Improved progress tracking consistency between backend and frontend
  - Better handling of indeterminate to determinate progress transitions

- **⚙️ Import and Dependency Issues**
  - Removed unused `get-port` ES module import causing startup failures
  - Cleaned up duplicate fs-extra imports
  - Improved module import organization

### Improved
- **🎯 Progress Tracking Accuracy**
  - More reliable progress updates during backup operations
  - Better ETA calculations and file transfer speed reporting
  - Clearer status messages throughout the backup process

- **🔄 Backend Stability**
  - Enhanced error handling in backup operations
  - Better logging for debugging backup issues
  - Improved status synchronization between frontend and backend

  
### 🐛 Known Bugs
- Google Drive Display in settings shows "Not Connected" on startup. Clicking "Test Connection" will temporarily fix the display.
- Automatic Software Update Download & Install is not fully implemented. For now, please use the "Manual Download" link to update.

## Coming Soon

### ✨ Planned Features & Improvements
- Feedback & Bug reporting Natively in the app
- Fully integrated Software Updates
- Improved Google Drive Integration
- Improved Disk Space Monitor
- Dashboard Improvements
- Canceling active Uploads

### Technical Changes
- Added `archiver` library for ZIP compression functionality
- Implemented `GoogleDriveStatusManager` for centralized status management
- Enhanced scheduled backup checking with minute-level precision
- Improved backup operation reference tracking with proper setId mapping

## [1.4.0] - 2025-05-20

### Added

- Implemented functional Inactivity Settings sliders that persist values.

### Fixed

- Corrected manifest file naming in backup destination to use user-specified name with .json extension.
- Ensured 'Sources' display correct information in Backup History.
- Fixed compiling/build issue related to file access during the build process (User needs to ensure the app is closed).

### Changed

- Modernized and vertically aligned toggle switch UI elements in Settings.
- Updated logo to a white cloud with a blue glow.

## [1.2.5] - 2025-03-20

### Fixed
- Fixed auto-update system to properly handle `latest.yml` file
- Resolved GitHub release integration issues
- Fixed update notification display in the UI

### Added
- Improved error handling for update process
- Better feedback during update checks
- Automated release publishing support

### Changed
- Updated electron-builder configuration for more reliable updates
- Improved documentation for release process
- Enhanced error messages for update failures

### Security
- Updated dependencies to latest stable versions
- Improved error handling for failed updates

## [1.2.0] - 2025-03-15

### Added
- Initial release with auto-update support
- Basic backup functionality
- Google Drive integration
- System tray support
- Dark/Light theme support

### Changed
- Improved UI/UX design
- Enhanced backup performance
- Better error handling

## [Latest] - Settings Page Redesign

### ✅ Complete Settings Page Redesign
- **Tabbed Interface**: 3 organized tabs (Security, Storage, Subscription)
- **Security Tab**: Notification settings + Inactivity configuration
- **Storage Tab**: Disk monitoring + Backup manifests management + Google Drive integration  
- **Tab Functionality**: Full JavaScript implementation with state persistence

### Features Added
- 🎨 Modern glassmorphic tab navigation with smooth animations
- 💾 LocalStorage state persistence - remembers last active tab
- ⌨️ Keyboard navigation support (Ctrl/Cmd + 1/2/3, Arrow keys)
- 📱 Fully responsive design with mobile-first approach
- ♿ Accessibility features (ARIA labels, high contrast, reduced motion)
- 🔄 Dynamic content loading per tab with performance optimization

### Technical Improvements
- Reorganized settings into logical grouped sections
- Enhanced visual hierarchy with color-coded section headers
- Improved grid layout for better content organization
- Added transition animations with respect for user motion preferences
- Integrated with existing settings APIs for seamless functionality

### User Experience Enhancements
- Cleaner, more intuitive navigation
- Better visual organization of related settings
- Consistent iconography across all tabs
- Hover effects and interactive feedback
- Smooth transitions between tab content

For detailed release notes, please visit the [GitHub releases page](https://github.com/IEver3st/CloudyV2-Releases/releases).
