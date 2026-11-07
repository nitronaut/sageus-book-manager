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
