add_swift_library(swiftPhotos ${SWIFT_SDK_OVERLAY_LIBRARY_BUILD_TYPES} IS_SDK_OVERLAY
  Photos.swift

  SWIFT_COMPILE_FLAGS "${SWIFT_RUNTIME_SWIFT_COMPILE_FLAGS}"
  LINK_FLAGS "${SWIFT_RUNTIME_SWIFT_LINK_FLAGS}"
  TARGET_SDKS IOS IOS_SIMULATOR TVOS TVOS_SIMULATOR
  SWIFT_MODULE_DEPENDS Foundation CoreLocation CoreImage CoreMedia
  SWIFT_MODULE_DEPENDS_IOS UIKit AVFoundation
  SWIFT_MODULE_DEPENDS_TVOS UIKit AVFoundation
  FRAMEWORK_DEPENDS Photos)

