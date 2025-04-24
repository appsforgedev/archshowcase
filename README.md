# 🍽 Architectures Showcase

Этот репозиторий демонстрирует различные архитектурные подходы и паттерны проектирования мобильных приложений на языке **Swift**.  
В качестве демонстрационного примера используется простое приложение с рецептами, включающее авторизацию, список рецептов, избранное и экран профиля.

> Цель — показать, как одни и те же фичи можно реализовать по-разному, сохраняя переиспользуемую бизнес-логику и UI-компоненты через модульную архитектуру.

---

## 📱 Функциональность демонстрационного приложения

- Авторизация по email / username и паролю
- Список рецептов с возможностью фильтрации по избранному
- Экран профиля с отображением логина и кнопкой выхода
- Детальный экран рецепта с возможностью добавить/удалить из избранного

---

## 🏗 Архитектурные подходы

| UI Framework | Архитектура                     | Статус         |
|--------------|----------------------------------|----------------|
| SwiftUI      | MVVM                             | ⏳ Not started ⭐ |
| SwiftUI      | TCA                              | ⏳ Not started ⭐ |
| SwiftUI      | Clean Architecture (custom DI)   | ⏳ Not started  |
| UIKit        | MVC                              | ⏳ Not started ⭐ |
| UIKit        | MVVM                             | ⏳ Not started  |
| UIKit        | VIPER                            | ⏳ Not started  |

> ⭐ — must-have варианты  
> ⏳ — ещё не начато

---

## 🧩 Структура проекта

Модульный монорепозиторий с использованием одного `Package.swift`.  
Каждый архитектурный пример импортирует только нужные зависимости.

```plaintext
ArchitecturesShowcase/
├── Package.swift
├── Modules/
│   ├── Shared/
│   │   ├── Models/
│   │   ├── Networking/
│   │   ├── TokenStorage/
│   │   ├── APIInterfaces/
│   │   ├── AppEnvironment/
│   │   └── UIComponents/
│   └── Features/
│       ├── Auth/
│       │   ├── Shared/
│       │   ├── SwiftUI/
│       │   │   └── MVVM/
│       │   └── UIKit/
│       │       └── MVC/
│       ├── RecipeList/
│       ├── RecipeDetail/
│       ├── Profile/
│       └── ...
├── App/
│   ├── App_MVVM_SwiftUI/
│   ├── App_TCA_SwiftUI/
│   ├── App_MVC_UIKit/
│   └── App_MVVM_UIKit/
│   └── ...
└── README.md
```

## ✅ Прогресс

### 🔧 Shared-модули

- [ ] Models
- [ ] Networking
- [ ] TokenStorage
- [ ] APIInterfaces
- [ ] UIComponents
- [ ] AppEnvironment

### 💡 Features (по фичам)

#### Auth
- [ ] Shared
- [ ] SwiftUI / MVVM
- [ ] UIKit / MVC

#### RecipeList
- [ ] Shared
- [ ] SwiftUI / MVVM
- [ ] UIKit / MVVM

#### RecipeDetail
- [ ] Shared
- [ ] SwiftUI / Clean Architecture
- [ ] UIKit / VIPER

#### Profile
- [ ] Shared
- [ ] SwiftUI / MVVM
- [ ] UIKit / MVC

### 🧪 Проекты-примеры

- [ ] App_MVVM_SwiftUI ⭐
- [ ] App_TCA_SwiftUI ⭐
- [ ] App_CLEAN_SwiftUI
- [ ] App_MVC_UIKit ⭐
- [ ] App_MVVM_UIKit
- [ ] App_VIPER_UIKit

> ⏳ Not started — задача ещё не начата  
> ✅ Done — задача завершена  
> 🕒 In progress — в процессе разработки  
> ⭐ — Must-have реализация


## 🧭 Навигация
Каждое демо-приложение имеет собственную точку входа и минимальную обвязку для запуска. Все демонстрации используют одни и те же данные, логики и модели, но с разными архитектурными подходами.

## 🧑‍💻 Участие
Проект открыт для предложений и PR. Если хочешь предложить свой паттерн или реализацию — welcome! Дать совет по любому из подходов, так же будем рады твоим идеям.