# openstack-config 

include $(TOPDIR)/rules.mk

PKG_NAME:=openstack-config
PKG_VERSION:=0.1
PKG_RELEASE:=2

include $(INCLUDE_DIR)/package.mk

define Package/openstack-config
  SECTION:=base
  CATEGORY:=Base system
  TITLE:=rc scripts to configure gluon instances
  DEPENDS:=+wget
endef

define Package/openstack-config/description
rc scripts to configure gluon instances. Generates fastd-key, enables fastd mesh-vpn, disables config mode
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile/Default
endef

define Build/Compile
	$(call Build/Compile/Default)
endef

define Package/openstack-config/install
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/openstack-configure $(1)/etc/init.d/
endef

$(eval $(call BuildPackage,openstack-config))
