# Architectures Showcase 🍏

**Демонстрация архитектурных подходов в iOS (SwiftUI & UIKit) с модульной SPM-структурой**

[![Swift 5.9](https://img.shields.io/badge/Swift-5.9-orange.svg)](https://swift.org)
[![Platform iOS 16+](https://img.shields.io/badge/Platform-iOS%2016%2B-blue)](https://developer.apple.com/ios/)

## 📌 О проекте

Проект демонстрирует реализацию одного приложения (менеджер рецептов) с использованием разных архитектурных паттернов, организованных как независимые SPM-пакеты. Каждый подход:
- Реализует одинаковый набор фич (авторизация, список рецептов, избранное)
- Использует общий `Core`-модуль
- Может быть подключен отдельно в другие проекты

## 🗺 Roadmap

### 🧩 Core Module (SPM)
```plaintext
[ ] Модели данных (Recipe, User)
[ ] Сетевой слой (APIService)
[ ] Локальное хранилище (FavoritesStorage)
```
---

## UIKit Реализации
Реализации на UIKit с разными архитектурными подходами:

### 📱 Доступные варианты
| Архитектура       | Статус       | Путь в репозитории          | Зависимости                  |
|-------------------|-------------|----------------------------|-----------------------------|
| **MVC**          | 🔴 Не начато | `Packages/UIKit-MVC`       | Core                        |
| **MVVM-Rx**      | 🔴 Не начато | `Packages/UIKit-MVVM-Rx`   | Core, RxSwift               |
| **MVVM-Closures**| 🔴 Не начато | `Packages/UIKit-MVVM-Closures` | Core                     |
| **VIPER**        | 🔴 Не начато | `Packages/UIKit-VIPER`     | Core                        |
| **Clean Swift**  | 🔴 Не начато | `Packages/UIKit-CleanSwift`| Core                        |

---

## SwiftUI Реализации
Реализации на SwiftUI с современными подходами:

### 🎨 Доступные варианты
| Архитектура       | Статус       | Путь в репозитории          | Зависимости                  |
|-------------------|-------------|----------------------------|-----------------------------|
| **MVVM**         | 🔴 Не начато | `Packages/SwiftUI-MVVM`    | Core                        |
| **MVVM-C**       | 🔴 Не начато | `Packages/SwiftUI-MVVM-C`  | Core                        |
| **TCA**          | 🔴 Не начато | `Packages/SwiftUI-TCA`     | Core, ComposableArchitecture|
| **Redux**        | 🔴 Не начато | `Packages/SwiftUI-Redux`   | Core, ReSwift               |
| **Actor Model**  | 🔴 Не начато | `Packages/SwiftUI-Actor`   | Core                        |


### Легенда:
    🟢 Готово
    🟡 В процессе
    🔴 Не начато

---

📦 Структура репозитория

```plaintext
├── Packages/
│   ├── Core/               # Общие модели и сервисы
│   ├── UIKit-MVVM/         # UIKit + MVVM реализация
│   ├── SwiftUI-TCA/        # SwiftUI + TCA реализация
│   └── ...
├── Apps/
│   ├── UIKit-MVVM-Demo/    # Демо-приложение для UIKit
│   ├── SwiftUI-TCA-Demo/   # Демо-приложение для SwiftUI
│   └── ...
├── Documentation/
└── README.md
```