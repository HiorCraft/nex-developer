# Surf-api

Die Surf-API ist eine der Hauptkomponenten des Nex Systems und bietet Funktionen für die Logik und Verwaltung von Projekten und Aufgaben. Sie ermöglicht es Entwicklern, benutzerdefinierte Funktionen und Erweiterungen für das Nex System zu erstellen.

## Funktionen der Surf-API

- **Projektverwaltung**: Erstellen, bearbeiten und löschen von Projekten.
- **Aufgabenverwaltung**: Erstellen, bearbeiten und löschen von Aufgaben innerhalb von Projekten
- **Benutzerverwaltung**: Verwalten von Benutzern und deren Berechtigungen innerhalb von Projekten.

## Installation der Surf-API

Füge anschließend in deiner `settings.gradle.kts` Datei die Abhängigkeit für surf-api hinzu:

```kotlin
pluginManagement {
    repositories {
        gradlePluginPortal()
        maven("https://repo.slne.dev/repository/maven-public/") { name = "maven-public" }
    }
}

plugins {
    id("org.gradle.toolchains.foojay-resolver-convention") version "1.0.0"
    id("dev.slne.surf.api.gradle.settings") version "<VERSION>"
}
```

In deiner `build.gradle.kts`, kannst du nun mit folgendem Codeblock direkt die Version aus deiner `gradle.properties` verwenden.

```kotlin
plugins {
    id("dev.slne.surf.api.gradle.core") version "<VERSION>"
}

group = "dev.slne.surf"
version = findProperty("version") as String
```

    