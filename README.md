# Featured Image - WordPress Plugin

[![WordPress Plugin Version](https://img.shields.io/badge/version-2.2-blue.svg)](https://wordpress.org/plugins/featured-image/)
[![WordPress Tested](https://img.shields.io/badge/WordPress-6.8-green.svg)](https://wordpress.org/)
[![License](https://img.shields.io/badge/license-GPL--2.0-orange.svg)](https://www.gnu.org/licenses/gpl-2.0.html)
[![Security Fix](https://img.shields.io/badge/security-CVE--2025--12019%20Fixed-success.svg)](SECURITY-FIX-SUMMARY.md)

Add featured images to any part of your WordPress website with ease. Provides shortcodes, widgets, and PHP functions for maximum flexibility.

## 🚨 Security Update v2.2

**CRITICAL**: Version 2.2 fixes a Stored Cross-Site Scripting (XSS) vulnerability (CVE-2025-12019). Please update immediately.

[View Security Fix Details](SECURITY-FIX-SUMMARY.md)

## Features

- ✅ **Easy Implementation** - Simple shortcode and widget
- ✅ **Flexible Display** - Use inside or outside the loop
- ✅ **Featured Image Caption** - Display image captions
- ✅ **Alt Text Support** - SEO-friendly with proper alt attributes
- ✅ **Secure** - Properly escaped output to prevent XSS
- ✅ **WordPress Standards** - Follows WordPress coding standards

## Installation

### From WordPress.org

1. Go to **Plugins → Add New**
2. Search for "Featured Image"
3. Click **Install Now** and then **Activate**

### Manual Installation

1. Download the plugin zip file
2. Extract the contents
3. Upload the `featured-image` folder to `/wp-content/plugins/`
4. Activate the plugin through the **Plugins** menu in WordPress

## Usage

### Shortcode

Display featured image in posts/pages:

```
[featured-img]
```

Display featured image caption:

```
[featured-img-caption]
```

### PHP Function

Use inside the loop in your theme:

```php
<?php if ( function_exists('get_featured_img') ) get_featured_img(); ?>
```

For caption:

```php
<?php if ( function_exists('get_featured_img_caption') ) get_featured_img_caption(); ?>
```

### Widget

1. Go to **Appearance → Widgets**
2. Find "Featured Image" widget
3. Drag it to your desired widget area
4. Configure and save

## Changelog

### Version 2.2 (2025-01-08) - Security Release

**Security Fixes:**
- Fixed Stored Cross-Site Scripting (XSS) vulnerability in image metadata (CVE-2025-12019)
- Added `esc_url()` for image URLs
- Added `esc_attr()` for alt text attributes
- Added `wp_kses_post()` for caption sanitization

**Bug Fixes:**
- Fixed missing `global $post` declaration in `getting_featured_img_caption()`
- Improved error handling to prevent PHP warnings

**Improvements:**
- Code refactored to use `sprintf()` for better readability
- Enhanced WordPress coding standards compliance
- Better null checks and validation

### Version 2.1
- Fixed global $post issue

### Version 2.0
- Added Featured Image Caption
- Added Alt Text for images
- Fixed various bugs

### Version 1.0
- Initial release

## Security

This plugin follows WordPress security best practices:

- ✅ All output is properly escaped
- ✅ Input is sanitized before use
- ✅ No SQL injection vulnerabilities
- ✅ No XSS vulnerabilities
- ✅ Follows WordPress coding standards

If you discover a security vulnerability, please email security@mer.vin

## Requirements

- WordPress 3.0 or higher
- PHP 5.6 or higher (7.4+ recommended)

## Support

- **WordPress.org Support**: [Plugin Support Forum](https://wordpress.org/support/plugin/featured-image/)
- **Documentation**: [Plugin Documentation](https://mer.vin/wordpress-featured-image)
- **Bug Reports**: [GitHub Issues](https://github.com/MervinPraison/featured-image/issues)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This plugin is licensed under the GPL v2 or later.

```
This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.
```

## Author

**Mervin Praison**
- Website: [mer.vin](https://mer.vin)
- Plugin URI: [WordPress Featured Image](https://mer.vin/wordpress-featured-image)

## Credits

- Security vulnerability discovered by: ZAST.AI
- Reported by: Wordfence

---

⭐ If you find this plugin useful, please consider leaving a review on [WordPress.org](https://wordpress.org/plugins/featured-image/)!
