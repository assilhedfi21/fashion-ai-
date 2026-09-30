# 👗 AI Fashion Advisor

Application Flutter qui permet de gérer sa garde-robe et recevoir des suggestions de tenues générées par IA.

## 🚀 Stack Technique

| Couche | Technologie |
|--------|-------------|
| UI | Flutter 3.x + Material 3 |
| State | Riverpod 2.x (StateNotifier, FutureProvider, StreamProvider) |
| Navigation | GoRouter |
| Persistance | Hive (local offline) |
| Auth | SharedPreferences (remplaçable par Firebase) |
| IA | Claude API / Anthropic |
| Météo | OpenWeatherMap API |
| Charts | fl_chart |

## 📦 Installation

```bash
flutter pub get
flutter run
```

## 🔑 Configuration des APIs

Éditer `lib/core/constants/api_constants.dart` :

```dart
static const String weatherApiKey = 'VOTRE_CLE_OPENWEATHER';
static const String claudeApiKey  = 'VOTRE_CLE_ANTHROPIC';
```

> Sans clés API, l'app fonctionne avec des données mock (météo et suggestions IA simulées).

## 🏗️ Architecture

```
lib/
├── core/           # Thème, couleurs, erreurs, réseau
├── models/         # ClothingItem, OutfitSuggestion, WeatherModel
├── services/       # Auth, Wardrobe, Weather, AI
├── providers/      # Riverpod providers
├── features/       # Pages par feature (auth, home, wardrobe, outfit, profile)
└── widgets/        # Widgets réutilisables
```

Clean Architecture + Feature-First + Riverpod.

## ✨ Fonctionnalités

- Authentification (email/password)
- Garde-robe virtuelle avec photos (caméra ou galerie)
- Filtrage par catégorie (hauts, bas, chaussures, accessoires)
- Suggestions de tenues par IA (Claude API)
- Météo locale intégrée
- Dashboard avec statistiques (PieChart)
- Mode sombre fashion
- Persistance offline (Hive)
