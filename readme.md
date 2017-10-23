In here I list software I like to use, mostly for my own benefit.


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


I am an Emacser. It allows me an extremely-customizable, portable environment,
with quite a lot of power. Also, it's what Dr. Bui told us to use at Penn
State Harrisburg on our first day of COMP 432, and it stuck.


I write plaintext files a lot. For simpler ones like readmes I tend to use
Markdown these days, and for more complex ones I lean towards reStructuredText.
Neither's perfect, but it beats reinventing the wheel.


If I want a SQL-accessible database, for local-app/prototyping purposes, I'll
tend to grab SQLite. For systems that need a Real Database, I favor PostGreSQL
for being open-source, robust, powerful, and for being zealous in its default
protection of my data integrity.


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
(selects, file inputs, radio buttons, and the like), Uniform.js is very handy.
http://uniformjs.com/


If you need a serious search engine for a website, Apache Solr is a very
powerful, fast full-text search engine built on Java, capable of importing
data from DBs, PDFs, and of doing faceted searches, as well as having some
geospatial search functions. It's not very user-friendly, and the architecture
is very Java, but it sure is fast.


If you have need of templating in PHP, Twig is the way to go, hands-down:
http://www.twig-project.org/


PHP Code Sniffer is a tool for detecting and fixing style violations in PHP
source code. You can define your own style guidelines.
https://github.com/squizlabs/PHP_CodeSniffer


httrack is a very cool tool for cloning websites for offline viewing that Bob
just introduced me to: http://www.httrack.com/


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


gitlist is a no-muss, no-fuss, nice little git repo viewer. It is looking like
my new go-to for such jobs. It's in PHP, so I've contributed a few patches.
https://github.com/klaussilveira/gitlist


Vagrant manages development environments, treating them as a collection of
1-to-N virtual machines.


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
screenshot/paste/eyedropper: http://instant-eyedropper.com/


http://typing.io/ A great little tool for exploring OSS code and learning to
type code (all those little weird characters, y'know?). Basic plans are free.


eslint is an excellent style-checker and linter for JS. Plugin architecture,
easily extensible, sane defaults, but everything configurable. http://eslint.org


Google Chrome is my preferred browser (for web development and general
browsing). A few useful plugins are worth noting here:
  * JSONView (make JSON responses prettier)
  * Edit This Cookie (edit cookies easily)
  * Swap My Cookies (store and exchange different sets of cookies)
  * Vimium (browse with vim-like keys)
  * Better History (make history easier to use and search)
  * The Great Suspender (save RAM/CPU by suspending inactive tabs)


crankd (part of https://github.com/nigelkersten/pymacadmin) is a great way to
kick off jobs on network connection/loss, on OS X. It'd be nice to write a
wrapper around it to let me schedule jobs for "when I have a connection again",
like scheduling git pushes for when I have a connection.
