include $(TOPDIR)/rules.mk

PKG_NAME:=xray-core
PKG_VERSION:=25.3.31
PKG_RELEASE:=1

PKG_SOURCE:=xray-$(PKG_VERSION).gz
PKG_SOURCE_URL:=https://github.com/pru79/pruhaha/raw/refs/heads/main/
PKG_HASH:=skip

PKG_MAINTAINER:=You <xray-core@xray-core.com>
PKG_LICENSE:=MPL-2.0

include $(INCLUDE_DIR)/package.mk

define Package/xray-core
  TITLE:=Xray-core Prebuilt Binary
  SECTION:=net
  CATEGORY:=Network
  URL:=https://github.com/XTLS/Xray-core
  DEPENDS:=+ca-bundle
endef

define Package/xray-core/description
  Xray, Penetrates Everything. Precompiled version for OpenWrt.
endef

define Package/xray-core/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(DL_DIR)/$(PKG_SOURCE) $(1)/usr/bin/xray.gz
	gzip -d $(1)/usr/bin/xray.gz
	chmod +x $(1)/usr/bin/xray
endef

$(eval $(call BuildPackage,xray-core))
