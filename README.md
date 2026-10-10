# CPVP Client (Fabric, Minecraft 1.21.11, singleplayer)

Samostatný klient (bez Meteoru): Crystal Aura, Anchor Aura, Auto Inv Totem.
Moduly běží POUZE v singleplayeru.

## Sestavení (Windows)
1. Nainstaluj JDK 21 (např. Temurin 21).
2. Gradle wrapper: otevři https://fabricmc.net/develop/template/ , vygeneruj libovolný
   projekt pro 1.21.11, rozbal ho a z něj zkopíruj do této složky:
   `gradlew`, `gradlew.bat` a složku `gradle/`.
3. V této složce: `gradlew.bat build`   (Linux/Mac: `./gradlew build`)
4. Hotový soubor: `build/libs/cpvp-client-1.0.0.jar` (NE ten s `-sources`).
5. Dej ho do `mods` v instanci Fabric 1.21.11 spolu s **Fabric API**.

## Použití (ve hře)
- `/cpvp`  otevře GUI s přepínači modulů
- `/cpvp toggle crystal-aura | anchor-aura | auto-inv-totem`
- `/cpvp set crystal-aura place-range 5`
- `/cpvp list`

## Poznámky
- Pokud Gradle nenajde verzi (loader/Fabric API/yarn), oprav ji v `gradle.properties`
  podle https://fabricmc.net/develop/ .
- Kód nebyl kompilován; případné chyby v názvech metod ukáže `gradlew build`.
