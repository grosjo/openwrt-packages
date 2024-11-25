#
# Copyright (C) 2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=tinytuya
PKG_VERSION:=1.15.1
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/jasonacox/tinytuya/archive/refs/tags/
PKG_HASH:=f05ec493e15146d13f547cda6a47eca95549c6be0b46fa7fcd63d01f90bf6925
PKG_BUILD_DEPENDS+=python-cryptography python-requests python-colorama python-charset-normalizer

PYPI_NAME:=tinytuya
PKG_MAINTAINER:=Jason Cox <jason@jasonacox.com>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-tinytuya
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Python module to interface with Tuya WiFi smart devices
  URL:=https://github.com/jasonacox/tinytuya
  DEPENDS+= \
	+python3-cryptography \
	+python3-requests \
	+python3-colorama \
	+python3-charset-normalizer
endef

define Package/python3-tinytuya/description
  This python module controls and reads state of Tuya compatible WiFi Smart Devices (Plugs, Switches, Lights, Window Covers, etc.) using the local area network (LAN) or the cloud (TuyaCloud API). This is a compatible replacement for the pytuya PyPI module and currently supports Tuya Protocols 3.1, 3.2, 3.3, 3.4 and 3.5.
  Tuya devices are designed to communicate with the TuyaCloud but most also expose a local area network API. This allows us to directly control the devices without using the cloud. This python module provides a way to poll status and issue commands to these devices.
endef

$(eval $(call Py3Package,python3-tinytuya))
$(eval $(call BuildPackage,python3-tinytuya))
$(eval $(call BuildPackage,python3-tinytuya-src))
