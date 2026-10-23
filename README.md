# Cat Emacs Scoop bucket

Windows installation for the Android Project and Compose Preview JVM CLIs:

```powershell
scoop bucket add java
scoop bucket add cat-emacs https://github.com/cat-emacs/scoop-bucket
scoop install cat-emacs/android-project cat-emacs/compose-preview
android-project doctor --json
compose-preview doctor --json
```

Requires an existing [Scoop](https://scoop.sh) installation. The Java bucket
provides the declared `temurin17-jdk` dependency. No Kotlin compiler or GitHub
Packages credentials are needed. Use a project-compatible `JAVA_HOME` when needed.

Manifests pin release archives and SHA-256 values. CI tests a real Scoop install,
command shims and doctor output on Windows; it does not claim full Android
rendering validation. WinGet/Chocolatey official catalog inclusion is not provided.

- [android-project](https://github.com/cat-emacs/android-project)
- [compose-preview](https://github.com/cat-emacs/compose-preview)
