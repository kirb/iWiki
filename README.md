# iWiki
## iPhone theme for MediaWiki
Version 2.2

## Discontinued
**This theme will not work with MediaWiki 1.17 or later,** instead it will just show the PHP error `Call to undefined method Skin::makeGlobalVariablesScript()`. I’ve decided to discontinue this as I don’t adminster a wiki any more. Try [Jony](https://github.com/Dialexio/Jony) instead, which you can preview live on [The iPhone Wiki](https://www.theiphonewiki.com/w/index.php?title=Main_Page&useskin=jony). This project will be kept up for archival purposes, or if someone wants to fork and continue it.

## Installation
1. `cd` to your MediaWiki's `skins` folder.
2. `git clone --recursive git://github.com/kirbylover4000/iWiki.git .`
3. `rm -rf .git README.md`
4. Open your `LocalSettings.php` and add the following code:  
```php
if (preg_match("/mobile|ipad|iphone|ipod|blackberry|opera mini|opera mobile|nokia|windows phone|android/i", $_SERVER['HTTP_USER_AGENT'])) {
	$wgDefaultSkin = "iwiki";
}
```
Optionally, you can also install a jQTouch theme to your `skins/iwiki/jqtouch/themes` folder and set it as default like so, changing `apple` to the theme you want:

```php
$wgTouchTheme = "apple";
```
5. Test on an iDevice. Enjoy ;)
