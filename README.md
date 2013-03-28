[PHPixie](http://phpixie.com) - [Twig](http://twig.sensiolabs.org/) Implementation
======================
About
-----------------------

**Twig** is a only-PHP template engine, fast (caches the results until the code or contents is modified),
secure (it has a sandbox mode to evaluate untrusted template code) and really flexible (allowing the developer
to define its own custom flags and filters).

Installation
------------------------

1. Download the repository, or clone it, or whatever, into your modules folder. You can delete the `README.md`.
2. Go to [Twig's Project Homepage](http://twig.sensiolabs.org/) and download the latest version of Twig.
3. Open the ZIP file and get into the `lib` folder. Copy the folder `Twig` into `modules/twig/vendor/`.
4. Does your final path look like this: `modules/twig/vendor/Twig`?
5. Cool. Go into `application/config/core.php` and add `twig` into your `modules` array.

Using it in PHPixie
----------------------

It's dead simple. Inside your controller, wherever you call the `View::get` static function, do the following:

1. Change `View` for `Twig`.
2. If you want cached results, write the following instead: `Twig::get("myview", true)`.
3. The last and also really important step, is that you must change your views formats to `.twig` instead of `.php` or anything else
