#
# Copyright (C) 2010-2013 hua.shao@mediatek.com
#
# Ralink Property Software.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ated
PKG_RELEASE:=1

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)
PKG_KCONFIG:=RALINK_MT7620 RALINK_MT7621 RALINK_MT7628
PKG_CONFIG_DEPENDS:=$(foreach c, $(PKG_KCONFIG),$(if $(CONFIG_$c),CONFIG_$(c)))


include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/kernel.mk

define Package/ated
  SECTION:=net
  CATEGORY:=Network
  TITLE:=ATE Daemon
endef

define Package/ated/description
  ATE Daemon
endef

define Build/Compile
endef

define Package/ated/install
	$(INSTALL_DIR) $(1)/bin
	$(INSTALL_BIN) ./ated $(1)/bin
endef


$(eval $(call BuildPackage,ated))

