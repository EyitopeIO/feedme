include $(TOPDIR)/rules.mk


PKG_NAME:=knemesis
PKG_SOURCE_URL:=https://github.com/EyitopeIO/knemesis.git
PKG_SOURCE_VERSION:=main
PKG_SOURCE_PROTO:=git
PKG_RELEASE:=1


include $(INCLUDE_DIR)/package.mk


define Package/knemesis
  SECTION:=Nextion
  DEPENDS:=+kmod-knemesisk
  TITLE:=Nextion display server
  URL:=https://github.com/EyitopeIO/knemesis
endef


define Package/knemesis/description
	Display server (compositor) for Nextion basic
endef


$(eval $(call BuildPackage,knemesis))
