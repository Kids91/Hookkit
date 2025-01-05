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

# Checkra1n
# Version: 1.0.2~13.7
# Depends: firmware (<< 15.0)

# Palera1n
# Version: 1.0.3~14.5
# Depends: firmware (>= 15.0)

export DEBUG				= 0
export GO_EASY_ON_ME		= 1
export THEOS_LEAN_AND_MEAN 	= 1
export FINALPACKAGE			= 1

include $(THEOS)/makefiles/common.mk

FRAMEWORK_NAME = RootBridge

RootBridge_FILES = RootBridge.m
RootBridge_INSTALL_PATH = /Library/Frameworks
RootBridge_CFLAGS = -fobjc-arc -IHeaders
RootBridge_LDFLAGS = -install_name /Library/Frameworks/RootBridge.framework/RootBridge
RootBridge_FRAMEWORKS = Foundation

include $(THEOS_MAKE_PATH)/framework.mk

# Depends: firmware (>=12.0) && firmware (<15.0)