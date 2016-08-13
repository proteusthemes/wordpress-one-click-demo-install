Deprecated in favor of [OCDI plugin](https://github.com/proteusthemes/one-click-demo-import).
====================================

---

One Click Demo Install for WordPress Developers
----------------------------------------------

*Note: original script written by https://github.com/FrankM1/radium-one-click-demo-install.*

This library works by importing wordpress content, widgets  and theme options with just one click.

### Requirements:

* WordPress Theme
* `content.xml` - generated using the Worpress Content Exporter plugin. Upload it to your server.
* `widgets.json` - generated using the Widget Importer Exporter plugin. Rename it from .wie to .json and upload it to your server.
* `theme_options.txt` - generated using the theme options frameworks such as Redux Framework, NHP Options Framework or Radium Framework

The new version v0.4.0 the script gets the demo data files (content.xml and widgets.json) from the server so you need to specify the URLs to these files:

```
public $content_demo_url = 'http://your_domain.com/path-to-file/content.xml';
public $widget_demo_url  = 'http://your_domain.com/path-to-file/widgets.json';
```

These files are then saved in the WordPress upload directory and used for demo import.


### How to use:

Add `require_once( get_template_directory() . '/wordpress-one-click-demo-install/example.php' );` to your theme's `function.php`.

Copy the files generated above into `demo-files/`.

Modify what menus need to be loaded in the `Radium_Theme_Demo_Data_Importer` class located in `examle.php` as well as the theme options name to be used.

A new menu should appear under ***Appearance &raquo; Import Demo Data***.

Click the import button.

That's it!
