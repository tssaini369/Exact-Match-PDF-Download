=== Exact Match PDF Download ===
Contributors: TeeJay
Tags: pdf, secure download, logging, shortcode, access control
Requires at least: 6.2
Tested up to: 6.8
Stable tag: 1.1
License: Proprietary Commercial License
License URI: file://license.txt

A secure WordPress plugin that allows logged-in users to download PDFs using exact document numbers, with encrypted URLs, activity logging, and an admin panel.

== Description ==
The Exact Match PDF Download plugin provides a secure way to distribute PDFs to authenticated users. It uses encrypted URLs to protect files, restricts access to logged-in users only, embeds PDFs for viewing, and logs all search and download activities. An admin panel allows monitoring of user interactions, and the plugin auto-sanitizes inputs for security.

Key Features:
- Encrypted URLs for secure PDF access.
- Restricted access for logged-in users only.
- Embedded PDF viewer with view/download options.
- Logging of search attempts, found status, and downloads.
- Admin panel to view logs (Time, Filename, IP Address, View, Downloaded).
- Automatic input sanitization and nonce security.

== Installation ==

### Exact PDF Download Plugin Setup

1. **Upload PDFs** via FTP/SFTP to:  
   `/wp-content/uploads/Product_COAs/`  
   - Files must be uppercase (e.g., `ABC-1234.PDF`)  
   - Folder is auto-created and protected by `.htaccess` during plugin activation to deny direct access.

2. **Install Plugin**  
   - Zip the `exact-pdf-download` folder  
   - Upload via WordPress Admin → Plugins → Add New → Upload Plugin → Install Now → Activate Plugin

3. **Usage**  
   - Add shortcode `[exact_pdf_search]` to any page to enable the search form.  
   - Users must be logged in to search and access PDFs.  
   - View logs in the `wp_epd_logs` database table or via the "EPD Logs" admin menu.

4. **Security**  
   - No configuration needed for Bluehost or other hosting providers.  
   - The plugin auto-sanitizes all inputs (e.g., filenames, file IDs) to prevent security vulnerabilities.  
   - Nonces are used for AJAX requests to protect against CSRF attacks.  
   - The `.htaccess` file in `/wp-content/uploads/Product_COAs/` ensures files cannot be accessed directly.

== Frequently Asked Questions ==

= Who can access the PDFs? =
Only logged-in users can search and access PDFs.

= What format should the PDF filenames be? =
Filenames must be uppercase (e.g., `ABC-1234.PDF`) and stored in `/wp-content/uploads/Product_COAs/`.

= How do I view the logs? =
Logs are stored in the `wp_epd_logs` table in your WordPress database. Admins can also view them via the "EPD Logs" menu in the WordPress dashboard.

= Is the plugin secure on Bluehost? =
Yes, no additional configuration is needed. The plugin handles security automatically with encrypted URLs, access restrictions, and sanitization.

== Screenshots ==

1. Search form on a page with embedded PDF viewer and buttons.
2. Admin panel showing search logs (Time, Filename, IP Address, Found, Downloaded).

== Changelog ==

= 1.1 =
* Updated license information.
* Added licensing terms reference to the `license.txt` file.

== Upgrade Notice ==

= 1.0 =
Initial release. No upgrades available yet.

== Additional Notes ==

- **Requirements**: PHP 5.6 or higher, WordPress 5.0 or higher.
- **Debugging**: Enable `WP_DEBUG` in `wp-config.php` to view logs in `wp-content/debug.log` for troubleshooting.
- **Limitations**: The plugin scans the PDF directory for decryption, which may slow down with many files. Consider indexing filenames in a database for large-scale use.
- **Support**: For issues, contact the author via the WordPress plugin repository or email.

== Usage ==
- The plugin requires a valid license to function.
- Activate a license via the Freemius opt-in prompt during plugin activation.

== Licensing ==
This plugin is distributed under a proprietary commercial license. Please refer to the `license.txt` file included in the plugin directory for full terms and conditions.
