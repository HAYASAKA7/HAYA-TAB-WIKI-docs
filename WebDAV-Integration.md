# WebDAV Integration

  Access your tab collection from cloud storage services that support WebDAV.

  ## Supported Services

  - ✅ Nextcloud
  - ✅ ownCloud
  - ✅ Synology NAS
  - ✅ Any standard WebDAV server
  - ⚠️ Chinese cloud services (Baidu, Alibaba) - may require special configuration

  ---

  ## Setup

  ### 1. Get Your WebDAV URL

  **Nextcloud/ownCloud:**
  https://your-server.com/remote.php/dav/files/USERNAME/

  **Synology:**
  https://your-nas-ip:5006/FOLDER/

  ### 2. Configure in HAYA-TAB

  1. Open **Settings** (⚙️ icon)
  2. Scroll to **WebDAV** section
  3. Enter:
     - **Server URL:** Your WebDAV endpoint
     - **Username:** Your account username
     - **Password:** Your account password
  4. Click **"Test Connection"**
  5. If successful, click **"Save"**

  ---

  ## Using Cloud Library

  ### Browse Files
  1. Click **"Cloud Library"** in the sidebar
  2. Navigate folders to find your tabs
  3. Supported files show a preview icon

  ### View Online
  - Click a file to open it directly in the viewer
  - File streams from cloud (not downloaded locally)
  - Perfect for large collections

  ### Download to Local
  - Right-click → **"Download"**
  - File is copied to your local library
  - Metadata is parsed and cover art fetched

  ### Upload to Cloud
  1. Right-click a local tab → **"Upload to WebDAV"**
  2. Select destination folder
  3. File is uploaded to your cloud storage

  ---

  ## Troubleshooting

  ### Connection Failed
  - Verify URL ends with `/`
  - Check username/password
  - Ensure WebDAV is enabled on your server
  - Try accessing the URL in a browser first

  ### Slow Loading
  - Large files may take time to stream
  - Consider downloading frequently-used tabs locally
  - Check your internet connection

  ### Chinese Cloud Services
  Some services (Baidu Netdisk, Alibaba Cloud) may:
  - Require app-specific passwords
  - Have rate limiting
  - Need special URL formats

  Check your provider's WebDAV documentation.

  ---

  ## Security

  - Credentials are stored locally with encryption
  - Passwords are never sent in plain text
  - Use HTTPS URLs when possible
  - Consider using app-specific passwords if available

  ---