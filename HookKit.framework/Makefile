THEOS_DEVICE_IP 		= 192.168.1.34
THEOS_DEVICE_PORT 		= 22

export ARCHS 		= arm64
# export SDKVERSION	= 13.7
# export SYSROOT		= $(THEOS)/sdks/iPhoneOS13.7.sdk
# export SDKROOT		= $(THEOS)/sdks/iPhoneOS13.7.sdk
# export TARGET		= iphone:clang:13.7:13.7
export SDKVERSION	= 14.5
export SYSROOT		= $(THEOS)/sdks/iPhoneOS14.5.sdk
export SDKROOT		= $(THEOS)/sdks/iPhoneOS14.5.sdk
export TARGET		= iphone:clang:14.5:14.5

ADDITIONAL_CFLAGS = -DTHEOS_SUPPORT_ROOTFUL=1

# Checkra1n
# Version: 1.0.16~13.7
# Depends: firmware (<< 15.0), me.jjolano.fmwk.modulous (<= 1.0.9), me.jjolano.fmwk.rootbridge (<= 1.0.2)

# Palera1n
# Version: 1.0.17~14.5
# Depends: firmware (>= 15.0), me.jjolano.fmwk.modulous (>> 1.0.9), me.jjolano.fmwk.rootbridge (>> 1.0.2)

export DEBUG				= 0
export GO_EASY_ON_ME		= 1
export THEOS_LEAN_AND_MEAN 	= 1
export FINALPACKAGE			= 1

include $(THEOS)/makefiles/common.mk

FRAMEWORK_NAME = HookKit

HookKit_FILES = Core.m Module.m Module+Internal.m Hook.m Compat.m
HookKit_FRAMEWORKS = Foundation Modulous RootBridge
HookKit_INSTALL_PATH = /Library/Frameworks
HookKit_CFLAGS += -F$(THEOS)/vendor/lib/Modulous.framework/Headers -F$(THEOS)/vendor/lib/RootBridge.framework/Headers

HookKit_LDFLAGS += -install_name /Library/Frameworks/HookKit.framework/HookKit
HookKit_LDFLAGS += -dynamiclib
HookKit_LDFLAGS += -rpath /Library/Frameworks -rpath /var/jb/Library/Frameworks -rpath /usr/lib -rpath /var/jb/usr/lib
HookKit_LDFLAGS += -F$(THEOS)/lib

include $(THEOS_MAKE_PATH)/framework.mk
