include $(TOPDIR)/rules.mk

PKG_NAME:=openwrt-public-dhcp-page

PKG_MAINTAINER:=Maciej Krüger <mkg20001@gmail.com>

include $(INCLUDE_DIR)/package.mk

define Package/openwrt-public-dhcp-page
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Routing and Redirection
  MAINTAINER:=Maciej Krüger <mkg20001@gmail.com>
  TITLE:=Public DHCP Lease Page
  URL:=https://github.com/realraum/openwrt-public-dhcp-page
  MENU:=1
  DEPENDS:=+luci-base +uhttpd
endef

define Package/openwrt-public-dhcp-page/install
  $(INSTALL_DIR) $(1)/www/cgi-bin/dhcp
  $(INSTALL_BIN) $(PKG_BUILD_DIR)/src/index.htm $(1)/www/cgi-bin/dhcp/
  $(INSTALL) $(PKG_BUILD_DIR)/src/index.htm $(1)/www/cgi-bin/dhcp/
  $(INSTALL_DIR) $(1)/www/cgi-bin/dhcp/json
  $(INSTALL_BIN) $(PKG_BUILD_DIR)/src/json/index.htm $(1)/www/cgi-bin/dhcp/json/
endef
