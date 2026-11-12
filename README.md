# sageus-book-manager
A book manager  plugin for wordpress.
=== Sageus Book Manager ===
Contributors: sageus
Tags: books, authors, bookstore, grid, widget
Requires at least: 6.2
Tested up to: 6.7
Requires PHP: 8.0
Stable tag: 1.0.2
License: GPLv2 or later

An easy-to-use system for authors to add books to their WordPress websites.

== Description ==
Adding books is as easy as filling out a form. Include as much or as little as you want: cover, purchase links, reviews, excerpt, and more.

* Each book gets its own page with a consistent look.
* Link each book to as many retailers as you want — affiliate links supported.
* Organize books into grids with a few clicks. Grids auto-update.
* Feature books in your sidebar: Random, Newest, Coming Soon (Future), or a Specific book.

== Installation ==
1. Upload the `sageus-book-manager` folder to `/wp-content/plugins/`.
2. Activate the plugin.
3. Go to Books → Add New to add your first book.
4. Go to Book Grids → Add New, copy the shortcode, and paste it into any page.
5. Go to Appearance → Widgets and add the Sageus Book Widget.

== Frequently Asked Questions ==
= Do I need to update grids when I add a book? =
No. Grids are rule-based and auto-update.

= Can I use affiliate links? =
Yes. Paste them exactly as your retailer gives them; they are stored verbatim.

== Changelog ==
= 1.0.0 =
* Initial release: Books CPT, Grids, Retailers, Widgets, Shortcodes, Blocks, Settings, Import/Export.

= 1.0.1 =
* FIX: Featured Image / Media Library — plugin declares post-thumbnails, enqueues wp.media on all edit screens, adds a dedicated Book Cover box that also sets Featured Image.
* FIX: Retailer & Purchase Links — repeater now uses a <template>, reindexes correctly, save no longer wipes links on autosave/quick-edit/REST, retailers page JS fixed.
* NEW: Details box on book pages + admin sidebar showing Published / Genres / Tags.
* FIX: Books/Grids use Classic Editor so meta boxes save reliably.
=======================================================

Done — v1.0.3:

**Download Sageus Book Manager v1.0.3 (.zip)**

### a] DETAILS moved above “Available at”

Order on the single book page is now:

1. Title / Author / Tagline
2. Meta list
3. **Details** — Published / Genres / Tags / ISBN / Publisher
4. **Available at** — retailer tiles
5. About / Excerpt / Reviews

Verified in the template: Details renders before `sageus_render_buy_buttons()`.

### b] “Available at” → horizontal tiles, 4 across, large retailer images

- **Layout:** CSS grid `repeat(4, minmax(0,1fr))` — max 4 across on desktop, 2 across on tablet/mobile, 2 across in the sidebar widget (compact mode)
- **Tile design:** White card, retailer-colour top border, centered:
  - **Large logo on top** — your Retailer Image URL, up to `100% wide × 72px tall`, `object-fit: contain` so logos aren't squashed. Previously it was a tiny 20px icon.
  - Retailer name underneath in bold
  - Custom label / format (e.g. “Paperback”) as a small subtitle — it no longer replaces the retailer name
  - “Buy →” CTA in the retailer colour
  - Hover lift + shadow
- **No logo?** Falls back to a large coloured tile with the retailer's initials in the retailer colour, same size — so the grid still looks even.

> To get the large logos: **Books → Retailers** → paste a logo URL in the **Button Image URL** column for each retailer → Save Retailers. Use a wide, transparent PNG if you have it (e.g. 600×200) — it will scale down cleanly. Logos already there will now just show much bigger.

### Install
Deactivate + delete old version (books are safe), then Plugins → Add New → Upload Plugin → v1.0.3 zip → Activate. Hard-refresh the book page once (`Ctrl+Shift+R`) so the new CSS loads.

Want the tiles to also show a price / format badge, or should the 5th+ retailer wrap to a second row of 4 (current behaviour) vs. staying on one scrollable row?
