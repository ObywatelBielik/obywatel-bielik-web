# Obywatel BIELIK Web

Repozytorium zawierające aplikację webową Obywatel BIELIK. Wersja webowa stanowi uzupełnienie aplikacji mobilnej i zapewnia dostęp do funkcjonalności projektu przez przeglądarkę.

## Opis projektu

Obywatel BIELIK to aplikacja służąca do gromadzenia opisów zdjęć (anotacji) przez społeczność, w tym seniorów i lokalnych aktywistów. Aplikacja umożliwia użytkownikom opisywanie losowych zdjęć lub dodawanie własnych zdjęć wraz z opisami.

## Struktura projektu

```
obywatel-bielik-web/
├── public/                 # Statyczne zasoby
│   ├── assets/             # Obrazy, ikony, fonty
│   └── index.html          # Główny plik HTML
├── src/                    # Kod źródłowy
│   ├── api/                # Integracja z API
│   ├── components/         # Komponenty wielokrotnego użytku
│   │   ├── common/         # Ogólne komponenty UI
│   │   ├── layout/         # Komponenty układu
│   │   └── features/       # Komponenty specyficzne dla funkcjonalności
│   ├── config/             # Konfiguracja aplikacji
│   ├── hooks/              # Niestandardowe hooki React
│   ├── models/             # Typy i interfejsy
│   ├── pages/              # Komponenty stron
│   ├── routes/             # Definicje tras
│   ├── services/           # Usługi (autentykacja, przechowywanie, itp.)
│   ├── store/              # Zarządzanie stanem (jjęśli używane)
│   ├── styles/             # Style i motywy
│   ├── utils/              # Narzędzia pomocnicze
│   ├── App.tsx             # Główny komponent aplikacji
│   └── index.tsx           # Punkt wejścia
├── tests/                  # Testy
│   ├── unit/               # Testy jednostkowe
│   ├── integration/        # Testy integracyjne
│   └── e2e/                # Testy end-to-end
├── .env.development        # Zmienne środowiskowe dla developmentu
├── .env.production         # Zmienne środowiskowe dla produkcji
├── package.json            # Zależności i skrypty
├── tsconfig.json           # Konfiguracja TypeScript
└── vite.config.ts          # Konfiguracja Vite
```

## Funkcjonalności aplikacji

Aplikacja webowa zapewnia wszystkie funkcjonalności dostępne w wersji mobilnej:

- Rejestracja i logowanie użytkowników (Google, Facebook, Apple)
- Wybór zespołu i konfiguracja profilu
- Strona startowa z:
  - Statystykami społeczności
  - Celem tygodniowym
  - Osiągnięciami użytkownika
  - Rankingami użytkowników i zespołów
- Opisywanie losowych zdjęć:
  - Wyświetlanie losowego zdjęcia
  - Generowanie automatycznego opisu
  - Dodawanie opisu narracyjnego i faktograficznego
  - Nagrywanie głosowe opisów
  - Korekta opisów przy pomocy AI
- Opisywanie własnych zdjęć:
  - Wybieranie zdjęć z dysku
  - Dodawanie opisów
- Zarządzanie kontem użytkownika

## Technologie

- **Framework:** React 18+
- **Język programowania:** TypeScript
- **Bundler:** Vite
- **Stylowanie:** Tailwind CSS
- **Zarządzanie stanem:** React Context API / Zustand
- **Routing:** React Router
- **Pobieranie danych:** React Query / SWR
- **Testowanie:** Jest, React Testing Library, Cypress
- **Formularze:** React Hook Form, Zod

## Wymagania deweloperskie

- Node.js 18+
- npm 8+ lub yarn 1.22+
- Nowoczesna przeglądarka (Chrome, Firefox, Safari, Edge)

## Ustawienie środowiska deweloperskiego

1. Sklonuj repozytorium:
```bash
git clone https://github.com/organization/obywatel-bielik-web.git
cd obywatel-bielik-web
```

2. Zainstaluj zależności:
```bash
npm install
# lub
yarn
```

3. Uruchom serwer deweloperski:
```bash
npm run dev
# lub
yarn dev
```

4. Otwórz `http://localhost:5173` w przeglądarce

## Konfiguracja środowiska

Aplikacja korzysta z plików `.env` dla różnych środowisk:
- `.env.development` - Środowisko deweloperskie
- `.env.test` - Środowisko testowe
- `.env.production` - Środowisko produkcyjne

## Testowanie

### Testy jednostkowe i integracyjne
```bash
npm test
# lub
yarn test
```

### Testy end-to-end
```bash
npm run cypress:open
# lub
yarn cypress:open
```

## Budowanie projektu

Aby zbudować wersję produkcyjną:

```bash
npm run build
# lub
yarn build
```

Zbudowana wersja zostanie umieszczona w katalogu `dist/`.

## Wdrażanie

Aplikacja jest przygotowana do wdrożenia na różnych platformach:

- **Netlify/Vercel:** Automatyczne wdrożenie po push do gałęzi main
- **Docker:** Użyj `Dockerfile` do zbudowania obrazu
- **Tradycyjny hosting:** Wystarczy przesłać zawartość katalogu `dist/`

## Dostępność

Aplikacja jest tworzona zgodnie ze standardem WCAG 2.2, aby zapewnić dostępność dla wszystkich użytkowników, w tym seniorów:

- Semantyczny HTML
- Pełna obsługa klawiatury
- Kompatybilność z czytnikami ekranu
- Odpowiednie kontrasty kolorystyczne
- Skalowalne rozmiary tekstu

## Wytyczne stylowania kodu

- Stosuj formatowanie Prettier
- Przestrzegaj reguł ESLint
- Używaj komponentów funkcyjnych i hooków React
- Pisz testy dla nowych komponentów i funkcjonalności

## Licencja

Projekt jest dostępny na licencji [licencja]. Szczegółowe informacje w pliku LICENSE.
