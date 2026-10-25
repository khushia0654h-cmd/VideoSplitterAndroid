# Video Splitter Android

Android 8+ app to split a video into 1/2/3/5/7/custom minute segments, preserving the last short part. Uses Android MediaExtractor and MediaMuxer, without re-encoding.

## Build APK without Android Studio
1. Create a new empty public or private GitHub repository.
2. Upload the CONTENTS of this ZIP, including `.github/workflows/build-apk.yml`, preserving directory paths. GitHub's web upload supports folders by dragging the extracted project directory's contents.
3. Open **Actions** > **Build APK** > **Run workflow** (or push to `main`).
4. When successful, open the run and download the `VideoSplitter-debug-apk` artifact ZIP. Extract `app-debug.apk` and install it on Android.

## Limitations
- Cuts happen on video keyframes, so split durations are approximate. All input samples are processed in order, but muxing may have boundary timestamp/audio synchronization issues on some devices. Validate results before relying on them.
- MP4 output only; some source codecs/containers may be unsupported.
- This project has not been built or tested in this environment. Debug APK is for personal testing, not Play Store release.
