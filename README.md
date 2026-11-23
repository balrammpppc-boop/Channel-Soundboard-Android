# Channel Soundboard - Android app (APK)

The same Channel Soundboard, packaged so that all its files are INSIDE the Android app (Capacitor).
No website, no address bar, works offline from the first start.

## Get the APK
1. Create a new Public repository on GitHub and upload: `www` folder, `assets` folder, `package.json`, `capacitor.config.json`, `debug.keystore`, `README.md`.
2. Create the file `.github/workflows/android.yml` (Add file -> Create new file) and paste the text of `android.yml` into it.
3. Actions tab -> **Build Android APK** -> Run workflow (about 5-10 minutes).
4. Open the finished run -> Artifacts -> **ChannelSoundboard-APK**. Unzip and install `ChannelSoundboard.apk`.
   (Pushing a tag such as `v8.1` also puts `ChannelSoundboard.apk` on the Releases page for a direct download.)

## Install on the phone
Allow "install unknown apps" for the app you open the file with (Files / Chrome), tap the APK, Install.
New builds install over the old one and keep your songs, because every build uses the same signing key (`debug.keystore`).

## Update the app
Replace `www/index.html` (and other changed files) in the repository and run the workflow again.

## Tips
- Settings -> Apps -> Channel Soundboard -> Battery -> **Unrestricted** so Android does not stop it in the background.
- Choosing a separate output device per channel is not available inside an Android app; use the Windows version for that.

## What is new in v10
Same app as the web version v10 (pages, clips, crossfade, song numbers).
