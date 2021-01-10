# tiktokvideodownloader


<html id="html"><head><meta http-equiv="Content-Type" content="text/html;charset=utf-8"><link id="baseCSS" href="https://markups.kdanmobile.com/mymarkup/front/the_components/reformat/base__newsprint.css" rel="stylesheet" class="newsprint" type="text/css"><style type="text/css" id="optionsCSS">#body { font-family: "PT Serif"; font-size: 16px; line-height: 1.5em; color: #1F0909; text-align: left; } #text { padding-top: 4.5em;padding-bottom: 9em;} #background { background-color: #FFFFFF; } .setTextColorAsBackgroundColor { background-color: #1F0909; } .setBackgroundColorAsTextColor { color: #FFFFFF; } .setBackgroundColor { background-color: #FFFFFF; } .setTextColor { color: #1F0909; } #box, .setBoxWidth { width: 36em; } a { color: #065588; } a:visited { color: #1F0909; } @media print { body.footnote_links__on_print a, body.footnote_links__on_print a:hover { color: #1F0909 !important; text-decoration: none !important; } } body.footnote_links__always a, body.footnote_links__always a:hover { color: #1F0909 !important; text-decoration: none !important; } img { border-color: #1F0909; } a img { border-color: #065588; } a:visited img { border-color: #1F0909; } h1 a, h2 a, a h1, a h2 { color: #1F0909; } h1, h2, h3, h4, h5, h6 { font-family: "PT Serif"; } pre { background-color: #FFFFFF; } pre, code { font-family: Inconsolata; } hr { border-color: #1F0909; } html.rtl #body #text { text-align: right !important; } h1, h2, h3, h4, h5, h6 { text-align: left; } html.rtl h1, html.rtl h2, html.rtl h3, html.rtl h4, html.rtl h5, html.rtl h6 { text-align: right !important; } #text div.separatorLine, #text section::before { background:      -o-linear-gradient(0, #FFFFFF 1%, #1F0909 50%, #FFFFFF 99%); background:    -moz-linear-gradient(0, #FFFFFF 1%, #1F0909 50%, #FFFFFF 99%); background: -webkit-linear-gradient(0, #FFFFFF 1%, #1F0909 50%, #FFFFFF 99%); } </style><link href="https://fonts.googleapis.com/css?family=PT+Serif:regular,bold,italic" rel="stylesheet" type="text/css"><link href="https://fonts.googleapis.com/css?family=Inconsolata:regular,bold,italic" rel="stylesheet" type="text/css"><link id="customFileCSS" href="https://markups.kdanmobile.com/mymarkup/front/the_components/reformat/custom__newsprint.css" rel="stylesheet" type="text/css"></head><body id="body" class="clearlyReady footnote_links__on_print large_graphics__do_nothing"><div id="curtains"></div><div id="bodyContent"><div id="box"><div id="box_inner"><div id="text"><div id="pages"><div class="page" id="page1"><div class="page_content"><div id="articleHeader"><h1 id="articleHeader__title">claudehohl/Stikked</h1><div id="articleHeader__separator" class="separator"><div class="separatorLine setTextColorAsBackgroundColor"></div></div></div>
    <div>
      <h2>
        README.md
      </h2>
    </div>
        

      
        <p>Stikked is an Open-Source PHP Pastebin, with the aim of keeping a simple and easy to use user interface.</p>
<p>Stikked allows you to easily share code with anyone you wish. Based on the <a href="http://code.google.com/p/stikked/" target="_blank">original Stikked</a> with lots of bugfixes and improvements.</p>
<p>Here are some features:</p>
<ul>
<li>Easy setup</li>
<li>Syntax highlighting for many languages, including live syntax highlighting with CodeMirror</li>
<li>Paste replies</li>
<li>Diff view between the original paste and the reply</li>
<li>An API</li>
<li>Search pastes</li>
<li>Trending pastes</li>
<li>Encrypted pastes</li>
<li>Burn on reading</li>
<li>Anti-Spam features</li>
<li>Themes support</li>
<li>Multilanguage support</li>
<li>Stikked client with support for client side encryption/decryption: <a href="https://github.com/tcolgate/gostikkit" target="_blank">gostikkit</a></li>
<li>Another CLI tool requiring only curl program: <a href="https://github.com/glensc/pbin" target="_blank">pbin</a></li>
<li>And many more. View <a href="http://maketecheasier.com/run-your-own-pastebin-with-stikked/2013/01/11" target="_blank">this review</a></li>
</ul>
<h2>Try it out</h2>
<p><a href="https://paste.scratchbook.ch/" target="_blank">https://paste.scratchbook.ch/</a></p>
<p>See an encrypted paste: <a href="https://paste.scratchbook.ch/view/1427473f#iP7p05DRH0BC72qQjxv01BjUeOmNV073" target="_blank">https://paste.scratchbook.ch/view/1427473f#iP7p05DRH0BC72qQjxv01BjUeOmNV073</a></p>
<h2>Prerequisites</h2>
<ul>
<li>A web server: Apache, Lighttpd, Nginx, Cherokee.</li>
<li>A database: MySQL, Postgres. OR a writable folder on your filesystem for SQLite.</li>
<li>PHP version 5.6 or newer is recommended.</li>
<li>PHP-GD for the creation of QR-codes.</li>
</ul>
<h2>Installation</h2>
<ol>
<li>Download Stikked from <a href="https://github.com/claudehohl/Stikked/releases" target="_blank">https://github.com/claudehohl/Stikked/releases</a></li>
<li>Create a user and database for Stikked</li>
<li>Copy application/config/stikked.php.dist to application/config/stikked.php</li>
<li>Edit configuration settings in application/config/stikked.php - everything is described there</li>
<li>You're done!</li>
</ol>
<ul>
<li>The database structure will be created automatically if it doesn't exist.</li>
<li>No special file permissions are needed by default. Optional: If you want to have the JavaScript- and CSS-files minified, the static/asset/ folder has to be writable.</li>
<li>To ensure that pastes with an expiration set get cleaned up, define the cron key in the config and set up a cronjob, for example:
<ul>
<li><code>*/5 * * * * curl --silent http://yoursite.com/cron/[key]</code></li>
</ul>
</li>
<li>If you encounter errors with stylesheets and paths, make sure your base_url config value is not empty (see <a href="http://www.codeigniter.com/user_guide/installation/upgrade_303.html" target="_blank">here</a>).</li>
<li>Be sure to also copy the .htaccess file when you move files around. This is a hidden file and easily overlooked.</li>
</ul>
<h2>How to run it in Docker</h2>
<pre><code>docker-compose up
</code></pre>
<p>This automatically builds the docker-image and fires up nginx, php and mariadb. Access your Stikked instance at <a href="http://localhost/" target="_blank">http://localhost/</a>.</p>
<p>All files are served directly; the Stikked-configuration for Docker resides in docker/stikked.php</p>
<h2>Documentation</h2>
<p>In the folder doc/, you will find:</p>
<ul>
<li>Webserver example configurations for Apache, Nginx, Lighttpd, Cherokee</li>
<li>A troubleshooting guide</li>
<li>How to create your own theme</li>
<li>How to translate Stikked into your language</li>
<li>How to contribute and improve Stikked</li>
</ul>
<h2>Changelog</h2>
<h3>Version 0.14.0:</h3>
<ul>
<li>Rewritten the Docker setup to be simple and clean:
<ul>
<li>switch to nginx-alpine, php-fpm-alpine and mariadb</li>
<li>docker-compose: autobuild php-image for stikked</li>
<li>serve all files directly (htdocs is mounted instead of copied)</li>
<li>stikked-configuration for docker resides in docker/stikked.php</li>
</ul>
</li>
<li>force private-flag when a previously encrypted paste gets pasted public</li>
<li>Fixed a critical bug that allowed pasting despite captcha</li>
<li>Various bugfixes and improvements</li>
</ul>
<h4>Upgrade instructions</h4>
<p>Copy your htdocs/application/stikked.php config file away. Upload the new version. Copy it back.</p>
<h3>Version 0.13.0:</h3>
<ul>
<li>Updated CodeIgniter to 3.1.9</li>
<li>Various improvements in the Docker setup</li>
<li>An automated Docker-build: <a href="https://hub.docker.com/r/claudehohl/stikked/" target="_blank">https://hub.docker.com/r/claudehohl/stikked/</a></li>
<li>Reverted the "intelligent language switcher" back to a fixed language setting because of too many side-effects</li>
<li>Fixed encodings and decryption functionality in various themes</li>
<li>Various bugfixes and improvements</li>
</ul>
<h4>Upgrade instructions</h4>
<p>Copy your htdocs/application/stikked.php config file away. Upload the new version. Copy it back.</p>
<p>The language setting in config/stikked.php is back, you can set a fixed language:</p>
<div><pre>$config['language'] = 'english';</pre></div>
<p>New config option: Content expiration. <br>
Sets the "Expires:"-header to make use of browser-caching <br>
Format: <a href="http://php.net/manual/en/function.strtotime.php" target="_blank">http://php.net/manual/en/function.strtotime.php</a> <br>
Examples: '+10 seconds', '+1 year', '-1 week' <br>
Browser-caching is disabled when this option is not set.</p>
<div><pre>$config['content_expiration'] = '+1 week';</pre></div>
<h3>Version 0.12.0:</h3>
<ul>
<li>Updates ensuring the compatibility with PHP7:
<ul>
<li>Updated CodeIgniter to 3.1.5</li>
<li>Updated GeSHi to 1.0.9.0</li>
</ul>
</li>
<li>Ability to run Stikked in Docker</li>
<li>Small security fixes regarding XSS and LDAP</li>
<li>Various bugfixes and improvements</li>
</ul>
<h4>Upgrade instructions</h4>
<p>Copy your htdocs/application/stikked.php config file away. Upload the new version. Copy it back.</p>
<p>If you want to keep QR codes being displayed, add the following line in config/stikked.php:</p>
<div><pre>$config['qr_enabled'] = true;</pre></div>
<h3>Version 0.11.0:</h3>
<ul>
<li>Upgrade to CodeIgniter 3.1.0</li>
<li>Added ACE editor</li>
<li>Ability to select JS editor (CodeMirror, ACE or none)</li>
<li>Insert paste text via drag &amp; drop</li>
<li>BBCode support</li>
<li>Improved Spamadmin; ability to delete single and multiple pastes at once</li>
<li>Soft api key</li>
<li>Lots of bugfixes and improvements</li>
</ul>
<h4>Upgrade instructions</h4>
<p>Copy your htdocs/application/stikked.php config file away. Upload the new version. Copy it back.</p>
<p>Add and set the base_url in htdocs/application/config/stikked.php</p>
<h3>Version 0.10.0:</h3>
<ul>
<li>Upgrade to CodeIgniter 3.0.1 and with it, lots of improvements:
<ul>
<li>SQLite support (yay!)</li>
<li>Lots of "Error 500" and blank screens fixed</li>
</ul>
</li>
<li>New theme: i386</li>
<li>New translations: Lithuanian, Danish, Polish</li>
<li>Automatic language detection</li>
<li>Support for the new ReCaptcha API</li>
<li>Support for Goo.gl and Bit.ly URL shorteners</li>
<li>Display expiration time if set</li>
<li>XSS fixes</li>
<li>Word wrap for looong words in paste display</li>
<li>And many more</li>
</ul>
<h4>Upgrade instructions</h4>
<p>Copy your htdocs/application/stikked.php config file away. Upload the new version.</p>
<p>Append the $config['expires'] part at the bottom of application/config/stikked.php.dist to your config.</p>
<p>Copy it back.</p>
<h3>Version 0.9.0:</h3>
<ul>
<li>New translations: Japanese, Chinese-Simplified, Chinese-Traditional, Russian</li>
<li>New themes: Stikkedizr, Cleanwhite</li>
<li>Display QR code in paste</li>
<li>Multiline highlighter</li>
<li>Encrypted pastes (yeah!) - see it in action: <a href="http://paste.scratchbook.ch/view/1427473f#iP7p05DRH0BC72qQjxv01BjUeOmNV073" target="_blank">http://paste.scratchbook.ch/view/1427473f#iP7p05DRH0BC72qQjxv01BjUeOmNV073</a></li>
<li>Added "burn on reading" as expiration</li>
<li>Search function - search in recent and trending pastes</li>
<li>Added mockingjay to word list for unknown posters - let the revolution begin!</li>
<li>Bugfixes and improvements</li>
</ul>
<h4>Upgrade instructions</h4>
<p>Copy your htdocs/application/stikked.php config file away. Upload the new version. Copy it back.</p>
<h3>Version 0.8.6:</h3>
<ul>
<li>New translations: Portuguese, Norwegian, Turkish, French</li>
<li>New theme: Snowkat</li>
<li>YOURLS support (<a href="http://yourls.org/" target="_blank">http://yourls.org/</a>)</li>
<li>There is now a stikked.php.dist. You may copy that to config.php and have your own settings</li>
<li>The API has more possibilities, see API doc</li>
<li>Captcha must be entered only once, no more for further pastes</li>
<li>Bugfixes and improvements</li>
</ul>
<h4>Upgrade instructions</h4>
<p>Copy your htdocs/application/stikked.php config file away. Upload the new version. Copy it back.</p>
<h3>Version 0.8.5:</h3>
<ul>
<li>Themes! Configure a different theme in config/stikked.php - or create your own</li>
<li>Multilanguage support. Configure a different language in config/stikked.php</li>
<li>Diff view for paste replies! View differences between the original paste and its reply</li>
<li>see it in action: <a href="http://paste.scratchbook.ch/view/de81a093/diff" target="_blank">http://paste.scratchbook.ch/view/de81a093/diff</a></li>
<li>Possibility to set default expiration time</li>
<li>Updated GeSHi to version 1.0.8.11</li>
<li>Updated CodeMirror to version 3.11</li>
<li>Lots of minor fixes and improvements</li>
<li>Added guides for troubleshooting, development, translation and creating themes</li>
<li>Added webserver example configurations</li>
<li>Added reCaptcha integration for better antispam</li>
</ul>
<h4>Upgrade instructions</h4>
<p>The following lines must be present config/stikked.php</p>
<div><pre>$config['theme'] = 'default';</pre></div>
<p>You can choose between default, bootstrap, gabdark, gabdark3 and a fancy geocities theme ;)</p>
<p>Create you own theme. See doc/CREATING_THEMES.md</p>
<div><pre>$config['language'] = 'english';</pre></div>
<p>You can choose between english, german and swissgerman ;)</p>
<p>Help translating Stikked into your language! See doc/TRANSLATING_STIKKED.md</p>
<h5>reCaptcha</h5>
<div><pre>$config['recaptcha_publickey'] = '';
$config['recaptcha_privatekey'] = '';</pre></div>
<p>If these lines are filled, reCaptcha will be used.
Get a key from <a href="https://www.google.com/recaptcha/admin/create" target="_blank">https://www.google.com/recaptcha/admin/create</a></p>
<h3>Version 0.8.4:</h3>
<ul>
<li>Trending pastes: <a href="http://paste.scratchbook.ch/trends" target="_blank">http://paste.scratchbook.ch/trends</a></li>
<li>LDAP authentication (thanks to Daniel, <a href="https://github.com/lightswitch05" target="_blank">https://github.com/lightswitch05</a>)</li>
<li>Blocked words; maintain a comma separated list in your config, e.g. '.es.tl, mycraft.com, yourbadword' - pastes with this words will never get pasted</li>
<li>Spam trap for bots</li>
<li>Bugfix: Remove_invisible_characters removing legitimate paste content (<a href="https://github.com/claudehohl/Stikked/issues/28" target="_blank">https://github.com/claudehohl/Stikked/issues/28</a>)</li>
<li>Possibility to manually set the paste's displayed URL (used with mod_rewrite configurations)</li>
<li>Print layout for pastes</li>
<li>Updated to CodeIgniter version 2.1.3</li>
</ul>
<h3>Version 0.8.3:</h3>
<ul>
<li>From now on, IPs get logged in the DB</li>
<li>Added spamadmin:
<ul>
<li>Enter credentials in config/stikked.php</li>
<li>Visit /spamadmin, login</li>
<li>Click on an IP to list all pastes belonging to it</li>
<li>You can remove all the pastes listed, and optionally block the IP range</li>
</ul>
</li>
<li>Updated to CodeIgniter version 2.1.2</li>
</ul>
<h3>Version 0.8.2:</h3>
<ul>
<li>Database optimizations: Pastes use less space (if you upgrade from a previous version, execute this SQL statement: "ALTER TABLE pastes DROP paste;"</li>
<li>Anti spam features:
<ul>
<li>Option to disable recent pastes</li>
<li>Option to require the user to enter a captcha</li>
</ul>
</li>
</ul>
<h3>Version 0.8.1:</h3>
<ul>
<li>Cleaner options</li>
<li>Valid RSS feed</li>
<li>Simpler API response (non-JSON)</li>
<li>Favicon</li>
<li>gw.gd URL shortener (replaces bit.ly)</li>
<li>Minor fixes</li>
</ul>
<h3>Version 0.8:</h3>
<ul>
<li>Added backup function (yoursite.com/backup; set credentials in stikked.php config)</li>
<li>Added pagination to the replies table</li>
<li>Added RSS-Feeds to recent pastes and paste replies</li>
<li>Embeddable pastes</li>
<li>GeSHi updated to version 1.0.8.10</li>
<li>Codemirror turned off by default</li>
<li>Codemirror: Syntax changes dynamically with selection in language dropdown</li>
</ul>
<h3>Version 0.7:</h3>

<h3>Version 0.6:</h3>
<ul>
<li>The language-selection was broken; the dropdown now features all the languages that GeSHi supports</li>
<li>Updated to CodeIgniter version 2.1.0</li>
<li>Creation of bit.ly-URLs (instead of snipurl)</li>
<li>Fixed download link</li>
<li>Paste downloads as a .txt file</li>
<li>No need to have PHP short tags enabled</li>
<li>Automatic creation of all necessary MySQL tables</li>
<li>Raw-mode is now like the raw-mode on pastebin.com</li>
<li>Minification and concatenation of CSS and JavaScript files (can be turned on/off)</li>
<li>Breached the license by removing the nasty copyright footer</li>
</ul>
<h3>Version 0.5:</h3>
<ul>
<li>Paste Replies</li>
<li>Fluid width pastes</li>
<li>Auto copying paste url to clipboard.</li>
<li>Paste expiration.</li>
<li>Fully standards compliant css and xhtml.</li>
<li>Random generating names for anonymous users</li>
<li>Paste downloading</li>
</ul>
</div></div></div><div id="footnotedLinks" class="separateSection"><div id="footnotedLinks__separator" class="separator"><div class="separatorLine setTextColorAsBackgroundColor"></div></div><ol id="footnotedLinks__list"><li><a href="http://code.google.com/p/stikked/">http://code.google.com/p/stikked/</a></li><li><a href="https://github.com/tcolgate/gostikkit">https://github.com/tcolgate/gostikkit</a></li><li><a href="https://github.com/glensc/pbin">https://github.com/glensc/pbin</a></li><li><a href="http://maketecheasier.com/run-your-own-pastebin-with-stikked/2013/01/11">http://maketecheasier.com/run-your-own-pastebin-with-stikked/2013/01/11</a></li><li><a href="https://paste.scratchbook.ch/">https://paste.scratchbook.ch/</a></li><li><a href="https://github.com/claudehohl/Stikked/releases">https://github.com/claudehohl/Stikked/releases</a></li><li><a href="http://www.codeigniter.com/user_guide/installation/upgrade_303.html">http://www.codeigniter.com/user_guide/installation/upgrade_303.html</a></li><li><a href="http://localhost/">http://localhost/</a></li><li><a href="https://hub.docker.com/r/claudehohl/stikked/">https://hub.docker.com/r/claudehohl/stikked/</a></li><li><a href="http://php.net/manual/en/function.strtotime.php">http://php.net/manual/en/function.strtotime.php</a></li><li><a href="http://yourls.org/">http://yourls.org/</a></li><li><a href="http://paste.scratchbook.ch/view/de81a093/diff">http://paste.scratchbook.ch/view/de81a093/diff</a></li><li><a href="https://www.google.com/recaptcha/admin/create">https://www.google.com/recaptcha/admin/create</a></li><li><a href="http://paste.scratchbook.ch/trends">http://paste.scratchbook.ch/trends</a></li><li><a href="https://github.com/lightswitch05">https://github.com/lightswitch05</a></li><li><a href="https://github.com/claudehohl/Stikked/issues/28">https://github.com/claudehohl/Stikked/issues/28</a></li></ol></div><div id="measure__lineHeight">Measure</div><div id="measure__fontSize">Measure</div></div></div></div><div id="background"><div id="background_shading"></div></div></div><link rel="stylesheet" href="https://markups.kdanmobile.com/mymarkup/front/the_components/reformat/style.css" type="text/css"></body></html>
