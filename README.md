# Android Module Generator

A minimal CLI tool to scaffold modular Android modules with standard Gradle

---

## ✨ Features

- Generate new modules in seconds
- Auto-create standard directory & package structure
- Generates a preconfigured `build.gradle.kts`
- Automatically updates your `settings.gradle.kts`
- Works out of the box with Kotlin DSL

## ⚙️ Usage

Make the script executable:
```bash
chmod +x android-module-generator.sh
```

Run the generator:
```bash
./android-module-generator.sh
```

You'll be prompted for:
- Base package (e.g. `com.yourapp.project`)
- Parent folder (e.g. `feature` or `core`)
- Module name (e.g. `home`)

The script then:
- Creates the full directory + package structure
- Adds a `build.gradle.kts` with common dependencies
- Updates your `settings.gradle.kts` with `include(":feature:home")`

## 🚀 Example

```
📦 Base package (example: com.project.app): com.example.app
📁 Parent folder (example: feature): feature
🧩 Module name (example: home): profile
```

Generates:

```
feature/
└── profile/
    ├── build.gradle.kts
    └── src/
        └── main/
            └── java/com/example/app/feature/profile
```

and automatically updates `settings.gradle.kts`.

## 📂 Requirements

- macOS/Linux (bash)
- Standard Android Gradle project using Kotlin DSL (`.kts`)

## 🙌 Credits

Created with ❤️ by [Luthfi Daffa Prabowo](https://linkedin.com/in/luthfi-daffa-prabowo)
