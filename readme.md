In here I list software I like to use, mostly for my own benefit.


I am an Emacser. It allows me an extremely-customizable, portable environment,
with quite a lot of power. Also, it's what Dr. Bui told us to use at Penn
State Harrisburg on our first day of COMP 432, and it stuck.


I write plaintext files a lot. For simpler ones like readmes I tend to use
Markdown these days, and for more complex ones I lean towards reStructuredText.
Neither's perfect, but it beats reinventing the wheel.


For writing software, my preferred language is Python. There are no good GUI
libraries for Python (or any language), as far as I can tell. I currently use
wxPython for cross-platform GUI development, in conjuncture with py2exe and
py2app. I use InnoSetup to create installers for py2exe packages.


pyenv lets you easily change the active Python version for a given project, and
helps you install the versions your apps need:
https://github.com/yyuu/pyenv


virtualenv is a Python tool for installing the modules required for a given
application in their own self-contained directory.
https://virtualenv.pypa.io/en/latest/


sqlmap.py is an excellent tool for showing people how deadly SQL injection
actually is. Not everyone realizes that you need no technical sophistication to
completely exploit a site with injection flaws, and this tool shows that
admirably. http://sqlmap.org/


If I want a SQL-accessible database, for local-app/prototyping purposes, I'll
tend to grab SQLite. For systems that need a Real Database, I favor PostGreSQL
for being open-source, robust, powerful, and for being zealous for my data's
integrity by default.


[Sass's SCSS syntax](http://sass-lang.com/) makes writing CSS less painful, by
giving you tools to keep things DRY. Be wary of the nesting feature, however -
it tends to lead to specificity wars.


jQuery is handy for simple DOM tweaking on basic pages.


For building/maintaining lists in websites where JS is allowed, this jQuery UI
plugin that modifies multiselects is decent (and I understand the codebase a
little, having contributed a patch or two):
https://github.com/crdeutsch/multiselect


When mail-client style autocompletion is desired in a web app, a different
jQuery UI plugin can be useful:
http://harvesthq.github.com/chosen/


When you want to apply pretty, customizable styles to tricky form elements
(selects, file inputs, radio buttons, and the like), Uniform.js is handy.
http://uniformjs.com/


If you have need of templating in PHP, Twig is the way to go, hands-down:
http://www.twig-project.org/ It's strongly inspired by Jinja, which is my
preferred templating language when in Python contexts: http://jinja.pocoo.org/


PHP Code Sniffer is a tool for detecting and fixing style violations in PHP
source code. You can define your own style guidelines.
https://github.com/squizlabs/PHP_CodeSniffer


httrack is a tool for cloning websites for offline viewing that Bob introduced
me to: http://www.httrack.com/ It was more relevant before the days of the SPA
came upon us.


I've decided to standardize my monospaced font, and Anonymous Pro is my
current victim: http://www.ms-studio.com/FontSales/anonymouspro.html


VirtualBox is an open-source app for virtualization. It runs nicely on OS X,
and is a decent (if slow) way to run MS Windows on Linux/OS X, or to play with
other operating systems.


[linkchecker](http://wummel.github.io/linkchecker/) is a simple tool for
checking websites for broken links. Excellent thing to run as part of a build
process, or just nightly against production, if you rely on links to other sites.


ievms is a handy script that does the painful work of making MS's IE testing
VMs work on Linux/OS X. You run it, you wait N hours, and you have a working
IE test setup. https://github.com/xdissent/ievms


iectrl is a program for managing the vms ievms creates. It is particularly
useful for re-installing the VMs after the Windows activation period has
expired. If you have not deleted the original downloads from ~/.ievms, you can
just do `iectrl reinstall 8`, and you'll have a working IE 8 VM in a minute or
three.


gitlist is a no-muss, no-fuss, nice little git repo viewer. It's in PHP, so
I've contributed a few patches. https://github.com/klaussilveira/gitlist


Vagrant manages development environments, treating them as a collection of
1-to-N virtual machines. It's primarily an abstraction over virtualization
platforms, letting developers think in terms like 'provision my box again',
'suspend my box', 'restart my box', etc. That mindset can be especially helpful
when hacking out provisioners to ensure consistency across environments.
https://www.vagrantup.com/


Ansible is a solid answer to the question "How do I define an app's execution
environment as a readable set of changes relative to a base OS image?"
https://www.ansible.com/


https://github.com/aehlke/tag-it is a pretty usable jQuery UI plugin for
tagging things. Low-muss, low-fuss. In an ideal world, this might be an
enhancement of a multiselect, a la Chosen, but practically speaking, it works
just fine.


http://digitalbush.com/projects/masked-input-plugin/ is a pretty usable jQuery
plugin for masking HTML input fields. Not usually a good idea, IMO, but it
does it about as well as I could ask for.


LogExpert is a decent Windows GUI for viewing/tailing logs:
http://logexpert.codeplex.com/


Instant EyeDropper is a Windows tool for getting any on-screen color. Not
flawless (only works on primary monitor), but sure beats
screenshot/paste/eyedropper: http://instant-eyedropper.com/ On OS X you can
just use the built in "Digital Color Meter" app.


http://typing.io/ A great little tool for exploring OSS code and learning to
type code (all those little weird characters, y'know?). Basic plans are free.


eslint is an excellent style-checker and linter for JS. Plugin architecture,
easily extensible, sane defaults, but everything configurable. http://eslint.org


Google Chrome is my preferred browser (for web development and general
browsing). It has some awesome built-in features, many of which can be
discovered by loading its list of internal URLS in a Chrome tab:
chrome://chrome-urls/

If you frequently use a URL with variable data somewhere in it, try setting it
up as a custom search engine at the chrome://settings/searchEngines URL. Once
you have, type your keyword, press tab, then enter the variable data. I think
of these as 'templated bookmarks'.

I use a slew of extensions with Chrome:

  * JSONView (make JSON responses prettier)
  * Edit This Cookie (edit cookies easily)
  * Swap My Cookies (store and exchange different sets of cookies)
  * Vimium (browse with vim-like keys)
  * Enhanced History (make history easier to use and search)
  * The Great Suspender (save RAM/CPU by suspending inactive tabs)
  * Custom Javascript for Websites (run arbitrary JS for arbitrary URLs)
  * Stylebot (user stylesheets since Chrome dropped built-in support)
  * GhostText (hook up your editor to Chrome textareas and see changes as you type)
  * New tab URL (redirect new tabs to a given URL [so vimium works on new tab])
  * StayFocusd (ration time on timewaster domains)
  * chrome-pass for hooking Chrome up to the 'pass' CLI password manager

It's handy to open chrome-pass via keyboard shortcut, but it doesn't have one
built-in. Fortunately, you can set custom keyboard shortcuts for extensions on
by clicking 'Keyboard shortcuts' at the bottom of the chrome://extensions page.
I use Command+Shift+L to trigger chrome-pass.


crankd (part of https://github.com/nigelkersten/pymacadmin) is a great way to
kick off jobs on network connection/loss, on OS X. It'd be nice to write a
wrapper around it to let me schedule jobs for "when I have a connection again",
like scheduling git pushes for when I have a connection.


iconv is a venerable tool for converting bytestreams from one character
encoding to another. It is thus useful for diagnosing character encoding
errors. If you feed it a document to convert from its claimed encoding to
another one, it will warn you if the document contains invalid byte sequences
for that encoding. It can also strip such byte sequences or replace them with a
placeholder of your choosing.


Audacity is a great basic audio recorder and editor, and it's open source.
Works for basic recording and effects processing (and I've used it for basic
sampling and audio mangling once or twice, in musical context).
https://www.audacityteam.org/


LilyPond is my preferred musical typesetting software. Entry requires
near-programmer levels of expertise with text, but its textual format allows me
to reuse pieces modularly in ways other typesetters I've seen don't. It also
allows for arbitrary control of layout and displayed typographical elements in
a way the others just don't. Some think it has more aesthetically pleasing
default output, which I don't know that I have an opinion on.
http://lilypond.org/


MuseScore is a very different piece of music typesetting software, far
friendlier to mortals (amazingly friendly, in fact). Its relevance to me is my
recent discovery that it has a MIDI notation entry system much like the one I
have fantasized about building for LilyPond. Since MuseScore can export
MusicXML, and there are several tools out there for converting MusicXML to
LilyPond format (search `xml2ly`), this might be a faster way for me to notate
parts when I'm arranging, while still eventually getting them into the LilyPond
format I know and love. https://musescore.org/en


Aria Maestosa is an open source (GPL v2) wxWidgets program for recording and
working with MIDI files. MIDI sequencing and recording has many uses, but one
application to which it can be put is exporting raw MIDI data for import into
MuseScore or Lilypond (importing MIDI is notoriously hard - gotta see which one
actually does better for me).
https://ariamaestosa.github.io/ariamaestosa/docs/index.html


MIDI Monitor is an open source tool for logging all MIDI events on OS X.
Probably mainly useful when debugging quirky hardware, but you never know what
it might come in handy for. https://www.snoize.com/MIDIMonitor/
