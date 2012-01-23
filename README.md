# iWiki
## iPhone theme for MediaWiki
Version 2.2
## Important
_This theme will **not** work with MediaWiki 1.17 or later, instead it will just show the PHP error `Call to undefined method Skin::makeGlobalVariablesScript()`. Stay tuned and watch this repo as an update will be coming soon._
## Installation
1. `cd` to your MediaWiki's `skins` folder.
2. `git clone git://github.com/kirbylover4000/iWiki.git .`
3. `git submodule init` then `git submodule update`
4. `rm -rf .git README.md`
5. Open your `LocalSettings.php` and add the following code:

	if (preg_match("/mobile|ipad|iphone|ipod|blackberry|opera mini|opera mobile|nokia|windows phone|android/i", $_SERVER['HTTP_USER_AGENT'])) {
            $wgDefaultSkin = "iwiki";
        }
    Optionally, you can also install a jQTouch theme to your `skins/iwiki/jqtouch/themes` folder and set it as default like so, changing `apple` to the theme you want:
        $wgTouchTheme = "apple";
6. Test on an iDevice. Enjoy ;)