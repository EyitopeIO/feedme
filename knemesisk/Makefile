include $(TOPDIR)/rules.mk


PKG_NAME:=knemesisk
PKG_SOURCE_URL:=https://github.com/EyitopeIO/knemesisk.git
PKG_SOURCE_VERSION:=main
PKG_SOURCE_PROTO:=git
PKG_RELEASE:=1


include $(INCLUDE_DIR)/kernel.mk
include $(INCLUDE_DIR)/package.mk


define KernelPackage/knemesisk
  SECTION:=Kernel modules
  TITLE:=Nextion display driver
  URL:=https://github.com/EyitopeIO/knemesisk
endef


define KernelPackage/knemesisk/description
  Kernel module for Nextion basic
endef


$(eval $(call KernelPackage,knemesisk))
