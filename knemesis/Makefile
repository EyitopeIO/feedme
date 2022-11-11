include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk
include $(INCLUDE_DIR)/KernelPackage.mk


PKG_NAME:=knemesis
PKG_SOURCE_URL:=https://github.com/EyitopeIO/knemesis.git
PKG_SOURCE_VERSION:=main
PKG_SOURCE_PROTO:=git
PKG_RELEASE:=1


include $(INCLUDE_DIR)/package.mk

define Package/knemesisk
  TITLE:=Nextion display driver
  DEPENDS:=+kmod-knemesis
  FILES:=$(PKG_BUILD_DIR)/knemesis.ko
endef

define Package/knemesisk/description
	Kernel module for Nextion Basic
endef



$(eval $(call Package,knemesisk))
