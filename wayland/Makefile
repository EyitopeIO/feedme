include $(TOPDIR)/rules.mk

PKG_NAME:=wayland
PKG_VERSION:=main
PKG_RELEASE:=1

PKG_MAINTAINER:=EyitopeIO <adeyitope.io@gmail.com>

PKG_BUILD_DEPENDS:= meson/host ninja/host

include $(INCLUDE_DIR)/host-build.mk

define Host/Install
	$(INSTALL_DIR) $(STAGING_DIR_HOSTPKG)/lib/meson
	$(CP) $(HOST_BUILD_DIR)/* $(STAGING_DIR_HOSTPKG)/lib/meson/
endef

define Host/Prepare
        mkdir -p $(HOST_BUILD_DIR)/wayland/
        git clone https://gitlab.freedesktop.org/wayland/wayland.git $(HOST_BUILD_DIR)/wayland
endef

define Host/Compile
	( \
		cd $(HOST_BUILD_DIR)/wayland && \
		$(STAGING_DIR_HOSTPKG)/lib/meson/meson.py $(HOST_BUILD_DIR)/wayland --prefix=$(HOST_BUILD_DIR)/wayland-tools ; \
		$(STAGING_DIR_HOSTPKG)/bin/ninja -C $(HOST_BUILD_DIR)/wayland install ; \
	)
endef

define Host/Clean
	rm -rf $(STAGING_DIR_HOSTPKG)/{libwayland,wayland}
	$(call Host/Clean/Default)
endef


$(eval $(call HostBuild))