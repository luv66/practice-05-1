# flutter-widgets-novitskyi

Flutter-додаток `mobile_widgets_app` з власними віджетами, анімаціями та state management (практична робота 5: «Розробка віджетів у Flutter»).

## Можливості
- Бібліотека custom-віджетів (Stateless + Stateful) з анімаціями
- Каталог товарів із shimmer-завантаженням, swipe-to-favorite, zoom зображення
- Кошик, обране, редагування профілю, світла/темна тема
- Showcase-екран: усі віджети з інтерактивними контролами та прикладами коду
- State management: `ChangeNotifier` + `provider`
- Unit-, widget- та flow-тести

## Вимоги
- Flutter SDK 3.16+ (Dart 3+)
- Android Studio або VS Code з Flutter extension
- Git

## Запуск
```bash
git clone https://github.com/<username>/flutter-widgets-novitskyi.git
cd flutter-widgets-novitskyi
flutter pub get
flutter run -d chrome      # web
flutter run                # Android-емулятор / телефон
```

## Тести та якість
```bash
flutter analyze
flutter test
flutter test --coverage    # coverage/lcov.info
```
Integration-тест (потрібен емулятор/пристрій): `flutter test integration_test`

## Збірка
```bash
flutter build web --release --base-href /flutter-widgets-novitskyi/
flutter build apk --release
```
Web-версія деплоїться на GitHub Pages або Firebase Hosting (див. docs/DEPLOY.md).

## Структура
```
lib/
├── main.dart
├── screens/   home, products, profile, showcase
├── widgets/   custom_button, profile_widget, animated_counter,
│              product_card, bounce_tap, shimmer
├── models/    user, product
└── utils/     constants, themes, app_state
test/          widgets/*, app_state_test, models_test, flows/app_flow_test
integration_test/
docs/          ARCHITECTURE.md, API_CONTRACT.md, DEPLOY.md
```

## Реалізовані віджети
| Віджет | Тип | Опис |
|---|---|---|
| `ProfileWidget` | Stateless | avatar, імʼя, email; compact/expanded, адаптивний, кольори з Theme |
| `CustomButton` | Stateless | 4 стилі (primary, secondary, danger, outline), іконка, стан loading |
| `AnimatedCounter` | Stateful | scale-анімація, зміна кольору на максимумі, bounce-кнопки, плавний progress |
| `ProductCard` | Stateful | swipe-to-favorite, zoom зображення, bounce-кнопка, анімована іконка «серце» |
| `BounceTap` | Stateful | обгортка з bounce-анімацією натискання |
| `Shimmer` / `ProductCardSkeleton` | Stateful | shimmer-ефект без сторонніх пакетів |

## Скріншоти
Додайте скріншоти в `docs/screenshots/` і вставте сюди:
`![Home](docs/screenshots/home.png)` `![Products](docs/screenshots/products.png)` `![Showcase](docs/screenshots/showcase.png)`

## Посилання
- Live demo: _додати посилання_
- Figma design system: _додати посилання_
- Відео-демо: _додати посилання_
- Діаграми архітектури: [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) / _draw.io посилання_
