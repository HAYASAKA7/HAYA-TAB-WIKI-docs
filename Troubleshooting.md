# Troubleshooting

  Common issues and solutions.

  ## Installation Issues

  ### Windows SmartScreen Warning
  **Problem:** "Windows protected your PC" message

  **Solution:**
  1. Click "More info"
  2. Click "Run anyway"
  3. This is normal for unsigned applications

  ### macOS "App is damaged" Error
  **Problem:** Cannot open because it's from unidentified developer

  **Solution:**
  ```bash
  # Remove quarantine attribute
  xattr -cr /path/to/HAYA-TAB.app

  # Or right-click → Open (first time only)
  ```

  ### Linux Permission Denied

  **Problem:** Cannot execute binary

  **Solution:**
  ```bash
  chmod +x HAYA-TAB-linux-amd64
  ./HAYA-TAB-linux-amd64
  ```

  ---

  ## Playback Issues

  ### No Sound in Guitar Pro Viewer

  **Possible causes:**
  1. SoundFont still loading (check progress bar)
  1. System volume muted
  2. Track is muted in the viewer

  **Solution:**
  - Wait for SoundFont to fully load
  - Check system audio settings
  - Click track selector and ensure track isn't muted

  ### Playback Stuttering

  **Possible causes:**
  1. Large file with many tracks
  2. System resources low

  **Solution:**
  - Close other applications
  - Try a simpler file first
  - Reduce playback speed

  ---

  ## Sync Issues

  ### Files Not Appearing After Sync

  **Possible causes:**
  1. Unsupported file format
  2. File in subdirectory (sync is not recursive by default)

  **Solution:**
  - Ensure files are `.pdf`, `.gp`, `.gp3`, `.gp4`, `.gp5`, `.gpx`, `.xml`, `.musicxml`, or `.mxl`
  - Move files to the root of sync folder
  - Click "Sync Now" again

  ### Duplicate Entries

  **Cause:** Same file synced multiple times

  **Solution:**
  - Duplicates are renamed with `_copy1`, `_copy2` suffix
  - Delete unwanted copies manually
  - Check sync paths for overlapping folders

  ---

  ## WebDAV Issues

  ### Connection Failed

  **Checklist:**
  - URL ends with `/`
  - Username/password correct
  - WebDAV enabled on server
  - Using HTTPS (not HTTP)
  - No firewall blocking

  **Test in browser:**
  ```
  https://your-server.com/remote.php/dav/files/username/
  ```

  ### Slow Cloud File Loading

  **Cause:** Large files streaming over network

  **Solution:**
  - Download frequently-used files locally
  - Check internet connection speed
  - Use wired connection if possible

  ---

  ## Database Issues

  ### Library Empty After Update

  **Cause:** Database migration issue

  **Solution:**
  1. Check `data/` folder for `.db` file
  2. If missing, restore from backup
  3. Report issue on GitHub with version info

  ### Search Not Working

  **Cause:** FTS5 index corruption

  **Solution:**
  1. Close HAYA-TAB
  2. Delete `data/haya-tab.db-wal` and `data/haya-tab.db-shm`
  3. Restart app (index rebuilds automatically)

  ---

  ## Performance Issues

  ### Slow Startup

  **Possible causes:**
  1. Large library (10,000+ tabs)
  2. Many sync paths
  3. Slow disk

  **Solution:**
  - First startup after update may be slow (migration)
  - Subsequent startups should be faster
  - Consider SSD if using HDD

  ### High Memory Usage

  **Cause:** Many tabs open or large cover art cache

  **Solution:**
  - Close unused viewer tabs
  - Clear cover cache: delete `covers/` folder
  - Restart application

  ---

  ## Still Having Issues?

  1. Check [GitHub Issues](https://github.com/HAYASAKA7/HAYA-TAB/issues) for similar problems
  2. Create a new issue with:
     - HAYA-TAB version
     - Operating system
     - Steps to reproduce
     - Error messages (if any)

  ---