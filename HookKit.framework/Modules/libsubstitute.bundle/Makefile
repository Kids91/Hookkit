THEOS_DEVICE_IP		= 192.168.1.34
THEOS_DEVICE_PORT	= 22

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
# Version: 1.0.11~13.7
# Pre-Depends: me.jjolano.fmwk.hookkit (<= 1.0.16)
# Depends: firmware (<< 15.0), mobilesubstrate, com.ex.substitute | com.ex.libsubstitute | science.xnu.substitute

# Palera1n
# Version: 1.0.12~14.5
# Pre-Depends: me.jjolano.fmwk.hookkit (>> 1.0.16)
# Depends: firmware (>= 15.0), mobilesubstrate, com.ex.substitute | com.ex.libsubstitute | science.xnu.substitute

export DEBUG				= 0
export GO_EASY_ON_ME		= 1
export THEOS_LEAN_AND_MEAN 	= 1
export FINALPACKAGE			= 1

include $(THEOS)/makefiles/common.mk

BUNDLE_NAME = HookKitSubstituteModule
HookKitSubstituteModule_BUNDLE_EXTENSION = bundle
HookKitSubstituteModule_FILES = Module.m HKSubstitute.m
HookKitSubstituteModule_LIBRARIES = _substitute
HookKitSubstituteModule_FRAMEWORKS = HookKit
HookKitSubstituteModule_EXTRA_FRAMEWORKS = _CydiaSubstrate
HookKitSubstituteModule_CFLAGS = -fobjc-arc -Ivendor/HookKit.framework/Headers
HookKitSubstituteModule_LDFLAGS = -rpath /Library/Frameworks -rpath /var/jb/Library/Frameworks -rpath /usr/lib -rpath /var/jb/usr/lib
HookKitSubstituteModule_LDFLAGS += -Fvendor -Lvendor/substitute
HookKitSubstituteModule_INSTALL_PATH = /Library/Modulous/HookKit

include $(THEOS_MAKE_PATH)/bundle.mk
