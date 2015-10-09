SUBDIRS = po

lscbindir = $(bindir)
lscbin_SCRIPTS = \
	lubuntu-software-center

lscsbindir = $(sbindir)
lscsbin_SCRIPTS = \
	scripts/lubuntu-software-center-build-db

lsclibscriptdir = $(pkgpyexecdir)
lsclibscript_SCRIPTS = \
        scripts/lubuntu-software-center-download-scrot \
	scripts/lubuntu-software-center-download-review

lscdir = $(pythondir)/LSC
lsc_PYTHON = \
	src/control.py \
	src/__init__.py \
	src/main.py \
	src/preferences.py \
	src/threadingops.py \
	src/UI.py \
	src/notify.py \
	src/testnet.py

lscwidgetsdir = $(pythondir)/LSC/widgets
lscwidgets_PYTHON = \
	src/widgets/__init__.py \
	src/widgets/appsinfo.py \
	src/widgets/basket.py \
	src/widgets/searchentry.py \
	src/widgets/toolbar.py \
	src/widgets/appsview.py \
	src/widgets/categories.py \
	src/widgets/pages.py \
	src/widgets/statusbox.py \
	src/widgets/screenshot.py

lscdatadir = $(datadir)/LSC
lscdata_DATA = \
	data/categories.ini \
	data/lsc.ui \
	data/preferences.ui

icon16dir = $(datadir)/icons/hicolor/16x16/apps
icon16_DATA = data/icons/16x16/lubuntu-software-center.png

icon24dir = $(datadir)/icons/hicolor/24x24/apps
icon24_DATA = data/icons/24x24/lubuntu-software-center.png

icon48dir = $(datadir)/icons/hicolor/48x48/apps
icon48_DATA = data/icons/48x48/lubuntu-software-center.png

icon128dir = $(datadir)/icons/hicolor/128x128/apps
icon128_DATA = data/icons/128x128/lubuntu-software-center.png

desktop_in_files = lubuntu-software-center.desktop.in 
desktop_DATA = $(desktop_in_files:.desktop.in=.desktop)
@INTLTOOL_DESKTOP_RULE@
desktopdir = $(datadir)/applications

ini_in_files = data/categories.ini.in 
ini_DATA = $(ini_in_files:.ini.in=.ini)
@INTLTOOL_DESKTOP_RULE@
inidir = $(lscdatadir)

dist_man_MANS = data/man/lubuntu-software-center.1 \
                data/man/lubuntu-software-center-build-db.1

CLEANFILES = \
	$(BUILT_SOURCES)
	
DISTCLEANFILES = \
	$(CLEANFILES)
	
EXTRA_DIST = \
        $(lscbin_SCRIPTS) \
        $(lscsbin_SCRIPTS) \
        $(lsclibscript_SCRIPTS) \
        $(lscdata_DATA) \
        $(lscman_DATA) \
        $(desktop_DATA) \
        $(desktop_in_files) \
        $(ini_DATA) \
        $(ini_in_files) \
        $(icon16_DATA) \
        $(icon24_DATA) \
        $(icon48_DATA) \
        $(icon128_DATA)

clean-local:
	rm -rf *.pyc *.pyo
