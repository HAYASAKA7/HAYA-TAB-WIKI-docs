# Tab Management

  ## Adding Tabs

  ### Upload Tab
  Copies the file into HAYA-TAB's internal `storage/` folder.

  1. Right-click on empty space → **"Upload TAB"**
  2. Select PDF, Guitar Pro, or MusicXML file(s)
  3. Metadata is auto-parsed from filename

  **Supported formats:** `.pdf`, `.gp`, `.gp3`, `.gp4`, `.gp5`, `.gpx`, `.xml`, `.musicxml`, `.mxl`

  **Best for:** Files you want HAYA-TAB to manage completely.

  ### Link Local Tab
  Creates a reference to an existing file without copying.

  1. Right-click → **"Link Local TAB"**
  2. Select your file

  **Best for:** Large collections you don't want to duplicate.

  ### Folder Sync
  Automatically imports all tabs from specified folders.

  1. Settings → Sync Paths → Add Path
  2. Select folder containing your tabs
  3. Click "Sync Now"

  **Sync Behavior:**
  - New files are added automatically
  - Duplicate titles get `_copy1`, `_copy2` suffixes (non-destructive)
  - Deleted files are NOT removed from library (manual cleanup required)

  ---

  ## Editing Metadata

  1. Right-click a tab → **"Edit"**
  2. Modify fields:
     - **Title** - Song name
     - **Artist** - Performer/band
     - **Album** - Album name
     - **Tags** - Version labels (e.g., "Lead", "Bass", "Acoustic")
  3. Click **"Save"**

  ### Auto-Metadata
  - **Filename parsing:** `Artist - Title.gp5` → Artist: "Artist", Title: "Title"
  - **Guitar Pro metadata:** When you open a GP file, internal metadata syncs back to the database
  - **Cover art:** Automatically fetched from iTunes based on artist/title

  ---

  ## Categories

  Categories are virtual folders for organizing tabs. A tab can exist in multiple categories.

  ### Create Category
  - Right-click → **"New Category"**
  - Or click the **"+"** button in Categories view

  ### Move Tabs to Category
  - Drag and drop tabs onto a category
  - Or right-click tab → **"Add to Category"** to add to a category
  - Or right-click tab → **"Remove from Category"** to remove from current category (not available for cloud storage category)

  ### Batch Operations
  1. Hold `Ctrl`/`Cmd` and click to select multiple tabs
  2. A batch action bar appears at the bottom
  3. Choose: **Move**, **Delete**, or **Cancel**

  ---

  ## Search

  The search bar supports instant full-text search:

  - **By Title:** `hotel california`
  - **By Artist:** `eagles`
  - **By Album:** `hell freezes over`
  - **Fuzzy matching:** `hotl califrnia` still finds "Hotel California"

  ### Search Filters
  Click the filter icon to narrow results:
  - **Type:** Song Name, Artist, Album, Tag
  - **Scope:** Current category or entire library

  ---