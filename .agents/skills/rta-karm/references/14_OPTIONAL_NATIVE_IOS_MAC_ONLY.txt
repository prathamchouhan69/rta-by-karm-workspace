# 14 — OPTIONAL: NATIVE iOS WRAPPER (ONLY ON A MAC WITH XCODE)

**Role.** iOS engineer. This is optional. The PWA is the product.

## Gate (step 0)
Run `uname -s`, `xcodebuild -version`, `xcrun simctl list devices available`. If not Darwin or Xcode is missing: write `reports/native/NATIVE_NOT_RUN.md` with the output and the sentence "No Mac with Xcode was available, so the native wrapper was not built. The PWA is the product." Set the prompt to `SKIPPED(no Mac)` and **stop**. That is a normal ending.

## Steps (only if the gate passes)
1. Capacitor in `apps/web` (`@capacitor/core`, `cli`, `ios`); display name exactly `Ṛta-BY-KARM`; same web build, no fork. Verify the built iOS display metadata preserves the exact spelling.
2. Plugins from official or well-maintained sources, versions recorded: Haptics, local biometrics (Face ID), Keyboard, Status Bar, Splash Screen, Share, Filesystem (PDFs), App lifecycle (lock). Use real plugins inside the wrapper (`Capacitor.isNativePlatform()`), PWA fallbacks outside. Session secret in the iOS Keychain, not localStorage.
3. Shell rules: portrait only; `NSFaceIDUsageDescription` with a clear reason; ATS on; no tracking; `PrivacyInfo.xcprivacy`; web inspector off in release; blank the view when inactive.
4. Stretch: Dynamic Island Live Activity showing "Syncing with Zoho" / "Sent" — words and counts only, never money. `SKIPPED` if time is short.
5. Apple tests: XCTest for the bridge (Keychain wrapper, lifecycle lock), XCUITest for launch → unlock → Today → quick create → draft.
6. Free install on the owner's own iPhone with an Apple ID; write `INSTALL_NATIVE.md` in plain words, noting free provisioning expires every 7 days.
7. `reports/native/NATIVE_REPORT.md`: what ran (with `xcresult` paths), what did not.

## Done means
- [ ] Gate recorded; either a tested wrapper or an honest skip.
