include $(TOPDIR)/rules.mk


PKG_NAME:=knemesis
PKG_SOURCE_URL:=https://github.com/EyitopeIO/knemesis.git
PKG_SOURCE_VERSION:=main
PKG_SOURCE_PROTO:=git
PKG_RELEASE:=1

PKG_BUILD_DEPENDS:=libffi/host meson/host meson-src/host wayland/host
HOST_BUILD_DEPENDS:=ninja/host


include $(INCLUDE_DIR)/package.mk

define Package/knemesis
	SECTION:=Nextion
	DEPENDS:=+kmod-knemesisk +libc +libstdcpp
	TITLE:=Nextion display server
	URL:=https://github.com/EyitopeIO/knemesis
endef

define Package/knemesis/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/knemesis $(1)/usr/bin/knemesis
endef

define Package/knemesis/description
	Display server (compositor) for Nextion basic
endef

$(eval $(call BuildPackage,knemesis))

