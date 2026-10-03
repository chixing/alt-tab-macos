# LocalPro personal build

LocalPro inherits Debug and defines `LOCAL_PRO`. It activates the existing in-memory Pro mock on every launch and does not initialize persisted licensing. Upstream Sparkle updates are disabled so they cannot replace this build.

Set your signing identity in the ignored `config/local.xcconfig`, then build:

```sh
xcodebuild -project alt-tab-macos.xcodeproj -scheme LocalPro -configuration LocalPro -derivedDataPath DerivedData CURRENT_PROJECT_VERSION=11.8.0
```

The app is at `DerivedData/Build/Products/LocalPro/AltTab.app`. Accessibility and Screen Recording permissions may need to be granted again for your signing identity.
