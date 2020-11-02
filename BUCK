
DEVELOPMENT_LANGUAGE = 'en'
EXECUTABLE_NAME = 'BuckTestObjC'
PRODUCT_NAME = 'BuckTestObjC'
PRODUCT_MODULE_NAME = 'BuckTestObjC'
PRODUCT_BUNDLE_IDENTIFIER = 'com.sbs.bucktestobjc'
PRODUCT_BUNDLE_PACKAGE_TYPE = 'APPL'

apple_asset_catalog(
    name = 'AppAssets',
    dirs = ['BuckTestObjC/Assets.xcassets'],
    app_icon = 'AppIcon',
)

apple_resource(
    name = 'AppResources',
    files = glob([
        'BuckTestObjC/*.storyboard'
    ])
)

apple_binary(
    name = 'AppBinary',
    srcs = glob([
        'BuckTestObjC/*.m'
    ]),
    headers = glob([
        'BuckTestObjC/*.h'
    ]),
    deps = [':AppAssets', ':AppResources'],
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework',
        '$SDKROOT/System/Library/Frameworks/UIKit.framework',
    ],
    configs = {
        'Debug': {
            "CONFIG_NAME": 'Debug',
            "DEVELOPMENT_LANGUAGE": DEVELOPMENT_LANGUAGE,
            "EXECUTABLE_NAME": EXECUTABLE_NAME,
            "PRODUCT_BUNDLE_IDENTIFIER": PRODUCT_BUNDLE_IDENTIFIER,
            "PRODUCT_NAME": PRODUCT_MODULE_NAME,
            "PRODUCT_MODULE_NAME": PRODUCT_MODULE_NAME,
            "PRODUCT_BUNDLE_PACKAGE_TYPE": PRODUCT_BUNDLE_PACKAGE_TYPE,
        },
        'Profile': {
            "CONFIG_NAME": 'Profile',
            "DEVELOPMENT_LANGUAGE": DEVELOPMENT_LANGUAGE,
            "EXECUTABLE_NAME": EXECUTABLE_NAME,
            "PRODUCT_BUNDLE_IDENTIFIER": PRODUCT_BUNDLE_IDENTIFIER,
            "PRODUCT_NAME": PRODUCT_MODULE_NAME,
            "PRODUCT_MODULE_NAME": PRODUCT_MODULE_NAME,
            "PRODUCT_BUNDLE_PACKAGE_TYPE": PRODUCT_BUNDLE_PACKAGE_TYPE,
        },
        'Release': {
            "CONFIG_NAME": 'Release',
            "DEVELOPMENT_LANGUAGE": DEVELOPMENT_LANGUAGE,
            "EXECUTABLE_NAME": EXECUTABLE_NAME,
            "PRODUCT_BUNDLE_IDENTIFIER": PRODUCT_BUNDLE_IDENTIFIER,
            "PRODUCT_NAME": PRODUCT_MODULE_NAME,
            "PRODUCT_MODULE_NAME": PRODUCT_MODULE_NAME,
            "PRODUCT_BUNDLE_PACKAGE_TYPE": PRODUCT_BUNDLE_PACKAGE_TYPE,
        },
    },
)

apple_bundle(
    name = 'App',
    binary = ':AppBinary',
    extension = 'app',
    product_name = PRODUCT_NAME,
    info_plist = 'BuckTestObjC/Info.plist',
    info_plist_substitutions = {
        "DEVELOPMENT_LANGUAGE": DEVELOPMENT_LANGUAGE,
        "EXECUTABLE_NAME": EXECUTABLE_NAME,
        "PRODUCT_BUNDLE_IDENTIFIER": PRODUCT_BUNDLE_IDENTIFIER,
        "PRODUCT_NAME": PRODUCT_MODULE_NAME,
        "PRODUCT_MODULE_NAME": PRODUCT_MODULE_NAME,
        "PRODUCT_BUNDLE_PACKAGE_TYPE": PRODUCT_BUNDLE_PACKAGE_TYPE,
    },
)

apple_package(
    name = 'AppPackage',
    bundle = ':App',
)
