# PR2 – Practical Work #2 (Node.js + TypeScript library)

## 📌 Опис
Це навчальна бібліотека на **TypeScript**, створена в рамках лабораторно-практичної роботи №2.  
Проєкт демонструє:
- роботу з `package.json`, залежностями та семантичним версіонуванням (SemVer);
- використання змінних оточення через `.env` + валідацію з `zod`;
- базові можливості TypeScript: типи, інтерфейси, класи, generics;
- налаштування інструментів розробки: **ESLint, Prettier, Husky, Commitlint**;
- поетапний розвиток коду від версії `0.1.0` до `2.0.0`.

---

## ⚙️ Інструкції з запуску

### Встановлення
```bash
git clone https://github.com/DenysKryvosheiev/PR2.git
cd PR2
npm install
```
## Крок 1. Ініціалізація проєкту

створено package.json, .gitignore, базові скрипти;

підключено eslint, prettier, husky, commitlint;

налаштовано tsconfig.json.
## Крок 2. Версія 0.1.0 – прості функції з any

реалізовано add(a: any, b: any) і capitalize(s: any);

продемонстровано відсутність перевірок при any;

eslint і prettier ловлять стилістичні помилки.

## Крок 3. Версія 0.2.0 – базові типи

ті ж функції, але вже з number і string;

з’явилися реальні помилки типів у demo.ts.

## Крок 4. Версія 0.3.0 – складний тип

додано type NumberFormatOptions;

функція formatNumber(value: number, options?: NumberFormatOptions).

## Крок 5. Версія 0.4.0 – інтерфейси + generics

створено інтерфейс User;

додано generic-функцію groupBy<T>(arr: T[], key: keyof T).

## Крок 6. Версія 0.5.0 – клас Logger + .env

створено файл src/config.ts з валідацією змінних через zod;

додано клас Logger з рівнями 'silent' | 'info' | 'debug';

formatNumber тепер бере значення з APP_PRECISION у .env.

## Крок 7. Версія 1.0.0 – стабілізація API

усі публічні експорти зібрані в src/index.ts;

посилено ESLint (заборонено any);

додано поля exports, main, module, types у package.json.

## Kрок 8. Версія 2.0.0 – breaking change

зміна сигнатури add: тепер приймає масив чисел add(values: number[]);

у demo.ts видно помилку компілятора й правильний виклик.
