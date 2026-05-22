=== SEO.LA IP Guard ===
Contributors: seola
Tags: security, login, ip restriction, admin protection
Requires at least: 5.0
Tested up to: 6.7
Stable tag: 1.0.0
License: GPL-2.0+

Restricts WordPress admin login to a whitelisted set of IP addresses. Built for NordLayer / dedicated IP VPN setups.

== Description ==

**SEO.LA IP Guard** adds a single, focused security layer: administrators can only log in from IP addresses you whitelist. Everyone else (editors, authors, subscribers) is completely unaffected.

**Built for:**
- Teams using a shared VPN with a dedicated IP (e.g. NordLayer / SEO.LA)
- Agencies managing multiple client WordPress sites
- Anyone who wants to prevent rogue admin logins without heavy security plugins

**Key features:**
- ✅ Restricts login for `administrator` role only
- ✅ All other roles unaffected
- ✅ Supports multiple IPs (one per line)
- ✅ Cloudflare & reverse-proxy aware (reads real client IP)
- ✅ Safety guard on activation — auto-adds your current IP
- ✅ "Add my current IP" button in settings
- ✅ Warns you if your IP isn't whitelisted before you save
- ✅ Zero dependencies, zero bloat (~150 lines of PHP)
- ✅ Free, forever

== Installation ==

1. Upload the `seola-ip-guard` folder to `/wp-content/plugins/`
2. Activate via **Plugins → Installed Plugins**
3. Go to **Settings → 🛡 IP Guard**
4. Your current IP is auto-added on activation — confirm it's your NordLayer IP, then save.

== Configuration ==

1. Connect to your NordLayer VPN to get your dedicated IP.
2. Go to **Settings → 🛡 IP Guard**.
3. Add the dedicated IP (one per line). Add all team member IPs if needed.
4. Save. Done.

To add a new team member: connect their VPN, check their IP appears under "Your current IP" on the settings page, and add it to the list.

== Frequently Asked Questions ==

= Will this lock out non-admin users? =
No. Editors, authors, subscribers, and all other roles can log in from any IP, always.

= What if I get locked out? =
Two options:
1. Connect via the VPN (NordLayer) — your whitelisted IP will then work.
2. Via cPanel/FTP: delete the plugin folder at `wp-content/plugins/seola-ip-guard/` to deactivate.

= Does it work behind Cloudflare or a reverse proxy? =
Yes. It checks `HTTP_CF_CONNECTING_IP` (Cloudflare) and `HTTP_X_REAL_IP` before falling back to `REMOTE_ADDR`.

= Can I use it on multiple sites? =
Yes, it's free with no license restrictions. Install on as many WP sites as needed.

== Changelog ==

= 1.0.0 =
* Initial release
