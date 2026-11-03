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
provides `temurin17-jdk` for Android Project and `temurin21-jdk` for Compose
Preview. Preview CLI/renderer require Java 21+; project Gradle JVM policy or
`--gradle-java-home` can select a different build JDK. No Kotlin compiler or
GitHub Packages credentials are needed.

Manifests pin release archives and SHA-256 values. CI tests a real Scoop install,
command shims and doctor output on Windows; it does not claim full Android
rendering validation. WinGet/Chocolatey official catalog inclusion is not provided.

- [android-project](https://github.com/cat-emacs/android-project)
- [compose-preview](https://github.com/cat-emacs/compose-preview)
