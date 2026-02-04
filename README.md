# 💰 NexusBlockMoney

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Minecraft](https://img.shields.io/badge/minecraft-1.21.8+-green.svg)
![Java](https://img.shields.io/badge/java-21+-orange.svg)
![Paper](https://img.shields.io/badge/paper-1.21.8+-red.svg)

**NexusBlockMoney** to zaawansowany plugin dla serwerów Minecraft BoxPVP, który zamienia standardowy system drop'ów z bloków na ekonomiczny system wypłat. Gracze otrzymują pieniądze bezpośrednio na konto zamiast fizycznych przedmiotów!

---

## ✨ Funkcje

- 🪙 **System wypłat za kopanie** - Gracze otrzymują pieniądze zamiast przedmiotów
- 💎 **Wsparcie dla wszystkich rud** - Coal, Iron, Gold, Diamond, Emerald, Ancient Debris i więcej
- ⛏️ **Integracja Fortune** - Automatyczne mnożniki dla kilofów z enchantem Fortune
- 🎨 **MiniMessage** - Nowoczesny system kolorów z gradientami
- 📝 **Konfigurowalne wiadomości** - Title i chat messages w pełni edytowalne
- 🔄 **Hot-reload** - Przeładuj konfigurację bez restartu serwera
- 🚀 **Wysoka wydajność** - Zoptymalizowany kod dla Java 21+
- 🔧 **Łatwa konfiguracja** - Dodawaj nowe bloki bez edycji kodu

---

## 📋 Wymagania

| Komponent | Minimalna wersja       |
|-----------|------------------------|
| **Paper** | 1.21.8+                |
| **Java** | 21+                    |
| **Vault** | 1.7.1+                 |
| **Plugin ekonomiczny** | EssentialsX, CMI, itp. |

> ⚠️ **Uwaga**: Plugin **wymaga** Vault oraz plugin ekonomiczny (np. EssentialsX) do działania!

---

## 📥 Instalacja
### Plugin dostepny do pobrania na strefie ultimate!!!

1. **Pobierz** najnowszą wersję z Dc [NexusDEV Mc | Hytale](https://discord.gg/KnMuqN6S)
2. **Umieść** plik `NexusBlockMoney.jar` w folderze `plugins/`
3. **Upewnij się**, że masz zainstalowane:
    - Vault
    - Plugin ekonomiczny (EssentialsX, CMI, etc.)
4. **Uruchom** serwer
5. **Skonfiguruj** plik `plugins/NexusBlockMoney/config.yml`
6. **Użyj** `/nexusblockmoney reload` lub uzyj alliasow: `/nbm` `/blockmoney` aby zastosować zmiany

---

## ⚙️ Konfiguracja

### config.yml

```yaml
# ========================================================================
#                  PLIK KONFIGURACYJNY: CONFIG.YML
#                   NexusBlockMoney | Wersja: 1.0
# ========================================================================

# Boost za każdy poziom Fortune (0.05 = 5% per poziom)
fortune-boost: 0.05

# Wiadomości (używają MiniMessage format)
messages:
  # Format title'a wyświetlanego nad hotbarem
  # Dostępne placeholdery: {amount}
  title-format: "<gradient:#00ff15:#00aa10>+{amount}$</gradient>"

  # Czy wysyłać dodatkową wiadomość na chat?
  chat-enabled: false

  # Format wiadomości na chacie
  # Dostępne placeholdery: {amount}, {block}
  chat-format: "<gray>[<gradient:#FFD700:#FFA500>BlockMoney</gradient>] <green>+{amount}$ <dark_gray>(<white>{block}</white>)</dark_gray>"

# ========================================================================
#                        KONFIGURACJA BLOKÓW
# ========================================================================
# Format: MATERIAL_NAME: wartość w $
# Wszystkie rudy z Minecraft 1.21+

blocks:
  # === WĘGIEL (COAL) ===
  COAL_ORE: 0.10
  DEEPSLATE_COAL_ORE: 0.12

  # === MIEDŹ (COPPER) ===
  COPPER_ORE: 0.15
  DEEPSLATE_COPPER_ORE: 0.18

  # === ŻELAZO (IRON) ===
  IRON_ORE: 0.25
  DEEPSLATE_IRON_ORE: 0.30

  # === ZŁOTO (GOLD) ===
  GOLD_ORE: 0.50
  DEEPSLATE_GOLD_ORE: 0.60

  # === LAPIS LAZULI ===
  LAPIS_ORE: 0.35
  DEEPSLATE_LAPIS_ORE: 0.40

  # === REDSTONE ===
  REDSTONE_ORE: 0.40
  DEEPSLATE_REDSTONE_ORE: 0.45

  # === DIAMENTY (DIAMOND) ===
  DIAMOND_ORE: 1.00
  DEEPSLATE_DIAMOND_ORE: 1.20

  # === SZMARAGDY (EMERALD) ===
  EMERALD_ORE: 1.50
  DEEPSLATE_EMERALD_ORE: 1.80

  # === NETHER - ZŁOTO ===
  NETHER_GOLD_ORE: 0.45

  # === NETHER - KWARC ===
  NETHER_QUARTZ_ORE: 0.30

  # === ANCIENT DEBRIS (NETHERITE) ===
  ANCIENT_DEBRIS: 5.00

  # === AMETYST ===
  AMETHYST_CLUSTER: 0.75
  LARGE_AMETHYST_BUD: 0.50
  MEDIUM_AMETHYST_BUD: 0.30
  SMALL_AMETHYST_BUD: 0.15

  # === BLOKI SUROWCÓW (Storage Blocks) ===
  COAL_BLOCK: 0.90
  COPPER_BLOCK: 1.35
  IRON_BLOCK: 2.25
  GOLD_BLOCK: 4.50
  LAPIS_BLOCK: 3.15
  REDSTONE_BLOCK: 3.60
  DIAMOND_BLOCK: 9.00
  EMERALD_BLOCK: 13.50
  NETHERITE_BLOCK: 45.00

  # === SUROWE SUROWCE (Raw Blocks) ===
  RAW_IRON_BLOCK: 2.00
  RAW_COPPER_BLOCK: 1.20
  RAW_GOLD_BLOCK: 4.00
