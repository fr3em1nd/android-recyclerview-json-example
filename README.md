# OTA-Exam

An Android application that displays exam levels and activities in a clean, scrollable list.

## Features

- Displays levels loaded from a JSON data source
- Shows level title, description, and state for each item
- Clean RecyclerView-based UI with View Binding
- Material Design 3 theming support

## Tech Stack

- **Language**: Kotlin
- **Min SDK**: 24 (Android 7.0)
- **Target SDK**: 33 (Android 13)
- **UI**: RecyclerView with View Binding
- **JSON Parsing**: Gson
- **Architecture**: Single Activity

## Project Structure

```
app/src/main/java/com/example/ota_exam/
├── MainActivity.kt      # Main entry point, loads and displays levels
├── Models.kt            # Data classes (LevelResponse, Level, Activity)
├── LevelAdapter.kt      # RecyclerView adapter for level items
└── ui/theme/            # Compose theming (Color, Theme, Type)
```

## Getting Started

### Prerequisites

- Android Studio Hedgehog (2023.1.1) or later
- JDK 8 or higher
- Android SDK with API level 34

### Build & Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd ota-exam
   ```

2. Open the project in Android Studio

3. Sync Gradle files

4. Run the app on an emulator or physical device:
   ```bash
   ./gradlew installDebug
   ```

### Building APK

```bash
# Debug build
./gradlew assembleDebug

# Release build
./gradlew assembleRelease
```

## Data Format

The app expects a `levels.json` file in the assets folder with the following structure:

```json
{
  "levels": [
    {
      "level": "1",
      "title": "Level Title",
      "description": "Level description",
      "state": "locked|unlocked|completed",
      "activities": [
        {
          "id": "activity-id",
          "challengeId": "challenge-id",
          "type": "quiz|lesson",
          "title": "Activity Title"
        }
      ]
    }
  ]
}
```

## License

This project is for educational purposes.
