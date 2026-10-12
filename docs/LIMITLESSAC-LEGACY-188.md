# LimitlessAC: Legacy 1.8.8 baseline

This branch is a GPL-3.0-compliant derivative of GrimAC (https://github.com/GrimAnticheat/Grim).
Keep the upstream LICENSE and original author notices. Modified files and additional commits document LimitlessAC changes.

## Target environment

- Server: PaperSpigot 1.8.8
- Current runtime: Java 8
- Upstream Grim 2.0: requires Java 17+ at runtime; do **not** deploy its current JAR on Java 8.
- Build JDK and Gradle versions must follow the upstream build documentation.

**Status:** Build and runtime compatibility have not been established. Changing plugin metadata does not make the fork Java 8-compatible.

## First change

The Bukkit plugin display name is changed to LimitlessAC. Internal Java packages, plugin main class, permission nodes and original author remain unchanged for compatibility. This is a metadata change only.

## Planned work

1. Obtain clean compile and test results for the unmodified Grim 2.0 Bukkit project.
2. Decide between migrating the server to a Java 17-compatible legacy fork or pinning an older Java 8-compatible Grim revision and backporting features.
3. Add a 1.8-specific test environment and record packet-processing and collision baselines.
4. Add reach evidence collection (no punishments or setbacks initially).
5. Verify with recorded legitimate gameplay and controlled test cases.

## Building (not Java 8 compatible yet)

On a supported build JDK, from the root:

```bash
./gradlew :bukkit:build
```

Windows:

```powershell
.\gradlew.bat :bukkit:build
```

Inspect the produced JAR and its dependencies, and deploy only to a disposable test server with a compatible runtime. Do not claim the fork is ready for production without passing these tests.

## Visibility

The fork repository is public. Do not commit secrets, private exploit signatures, credentials, or personal data.
