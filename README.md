# EcoTycoon - Gra Ekologiczna

EcoTycoon to interaktywna gra symulacyjna, w której zarządzasz fabrykami i oczyszczalniami powietrza, aby kontrolować zanieczyszczenie i zarabiać pieniądze. Celem gry jest znalezienie równowagi między rozwojem gospodarczym poprzez rozbudowę fabryk a zarządzaniem poziomem zanieczyszczenia przy pomocy oczyszczalni powietrza. Gra została zbudowana przy użyciu Flaska, SQLAlchemy i bazy danych SQLite.

## Funkcje

- **Zarządzanie stanem gry**: Gra zapisuje stan gry, w tym siatkę, poziom zanieczyszczenia i pieniądze, w bazie danych.
- **Fabryki**: Buduj fabryki na siatce, aby zarabiać pieniądze, ale pamiętaj, że fabryki generują zanieczyszczenie.
- **Oczyszczalnie powietrza**: Buduj oczyszczalnie powietrza, aby usuwać zanieczyszczenie i dbać o czyste środowisko.
- **Ulepszanie**: Ulepszaj fabryki i oczyszczalnie powietrza, aby zwiększyć ich efektywność i dochody.
- **Dynamiczna siatka**: Siatka o wymiarach 32 kafelków, na której możesz budować i ulepszać fabryki i oczyszczalnie powietrza.
- **Postęp gry**: Twoim celem jest zarządzanie równowagą między pieniędzmi, zanieczyszczeniem a budową fabryk i oczyszczalni powietrza.

## Technologie

- **Flask**: Framework webowy dla Pythona.
- **SQLAlchemy**: ORM do zarządzania bazą danych.
- **SQLite**: Lekka relacyjna baza danych.
- **HTML/CSS**: Dla interfejsu użytkownika.
- **JavaScript (jQuery)**: Do aktualizacji stanu gry w czasie rzeczywistym.

## Instalacja

Aby uruchomić grę na swoim lokalnym komputerze, wykonaj poniższe kroki:

### Wymagania wstępne

1. Python 3.x
2. Flask
3. SQLAlchemy
4. SQLite (zwykle wbudowane w Pythona)

### Kroki

1. **Sklonuj repozytorium**:

    ```bash
    git clone <repository-url>
    cd eco-tycoon
    ```

2. **Utwórz wirtualne środowisko** (zalecane, ale nie obowiązkowe):

    ```bash
    python -m venv venv
    source venv/bin/activate   # Na Windows: venv\Scripts\activate
    ```

3. **Zainstaluj wymagane zależności**:

    ```bash
    pip install -r requirements.txt
    ```

    Jeśli nie masz pliku `requirements.txt`, możesz zainstalować Flask i SQLAlchemy ręcznie:

    ```bash
    pip install Flask SQLAlchemy
    ```

4. **Uruchom aplikację**:

    ```bash
    python app.py
    ```

    Aplikacja powinna teraz działać na `http://127.0.0.1:5000/`.

## Jak grać

1. **Przegląd gry**:
    - Gra zaczyna się od 32-kafelkowej siatki, na której możesz budować fabryki i oczyszczalnie powietrza.
    - Fabryki generują dochód, ale również zwiększają zanieczyszczenie.
    - Oczyszczalnie powietrza redukują zanieczyszczenie wytwarzane przez fabryki.
    - Zarabiasz pieniądze, ulepszając fabryki i zarządzając zanieczyszczeniem.

2. **Budowanie i ulepszanie**:
    - **Budowa fabryki**: Kliknij na pusty kafelek i zdecyduj się na budowę fabryki za 500 zł.
    - **Budowa oczyszczalni powietrza**: Kliknij na pusty kafelek i zdecyduj się na budowę oczyszczalni powietrza za 300 zł.
    - **Ulepszanie fabryki**: Kliknij na fabrykę i zdecyduj się na jej ulepszenie. Koszt ulepszenia rośnie z każdym poziomem.
    - **Ulepszanie oczyszczalni powietrza**: Kliknij na oczyszczalnię i ulepsz ją, aby zwiększyć jej wydajność w usuwaniu zanieczyszczeń.

3. **Zarządzanie zanieczyszczeniem**:
    - Zanieczyszczenie rośnie co sekundę w zależności od liczby fabryk.
    - Zanieczyszczenie zmniejsza się, gdy budujesz lub ulepszasz oczyszczalnie powietrza.
    - Jeśli poziom zanieczyszczenia osiągnie zero, będzie się zwiększać po każdej inkrementacji.

4. **Status gry**:
    - Gra wyświetla aktualny stan pieniędzy i poziom zanieczyszczenia na górze ekranu.
    - Siatka pokazuje wszystkie fabryki i oczyszczalnie powietrza, a także umożliwia interakcję z nimi.

5. **Aktualizacje w czasie rzeczywistym**:
    - Gra aktualizuje status co sekundę, wyświetlając aktualne dane dotyczące pieniędzy i zanieczyszczenia.
