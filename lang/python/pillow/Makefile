#
# Copyright © 1997-2011 by Secret Labs AB
# Copyright © 1995-2011 by Fredrik Lundh
# Copyright © 2016 by Alex Clark and contributors
#

include $(TOPDIR)/rules.mk

PKG_NAME:=pillow
PKG_VERSION:=9.4.0
PKG_RELEASE:=1

PYPI_NAME:=Pillow
PKG_HASH:=a1c2d7780448eb93fbcc3789bf3916aa5720d942e37945f4056680317f1cd23e

PKG_MAINTAINER:=Alexandru Ardelean <ardeleanalex@gmail.com>
PKG_LICENSE:=HPND
PKG_LICENSE_FILES:=LICENSE
PKG_CPE_ID:=cpe:/a:python:pillow

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-pillow
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=The friendly PIL fork
  URL:=https://python-pillow.org/
  DEPENDS:=+libfreetype +libjpeg +libtiff +zlib \
	   +libwebp +python3
endef

define Package/python3-pillow/description
  The friendly PIL fork
endef

PYTHON3_PKG_SETUP_GLOBAL_ARGS += build_ext \
	--enable-zlib \
	--enable-jpeg \
	--enable-webp \
	--enable-webpmux \
	--enable-tiff \
	--enable-freetype \
	--disable-lcms \
	--disable-jpeg2000 \
	--disable-imagequant \
	--disable-platform-guessing

$(eval $(call Py3Package,python3-pillow))
$(eval $(call BuildPackage,python3-pillow))
$(eval $(call BuildPackage,python3-pillow-src))
