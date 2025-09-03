
# COVID-19 Database & Analysis  

Projekt bazy danych i analizy COVID-19 oparty na danych z **World Data Bank / WHO**, pobranych **17 sierpnia 2025**.  
Dodatkowo została utworzona kolumna **daily cases (~weekly/7)** w celu oszacowania liczby dziennych przypadków.  

---

## 📂 Struktura repozytorium  

### `data/` – Dane źródłowe  
- **`weekly-covid-cases.csv`** – tygodniowe potwierdzone przypadki COVID-19 (Our World in Data / WHO)  
- **`weekly-covid-cases.json`** – informacje w formacie JSON  
- **`daily-cases-estimated.csv`** – dane pobrane z World Data Base dot. zakażeń COVID-19

### `sql/` – Skrypty bazodanowe  
- **`START.SQL`** – skrypt inicjalizujący strukturę bazy danych  
- **`KOMENDY.SQL`** – przykładowe zapytania SQL  
- **`WIDOKI.SQL`** – definicje widoków do analizy  

### `bi/` – Wizualizacje i raporty  
- **`covid-19.pbix`** – dashboard w Power BI  
- **`covid-19.pdf`** – raport końcowy  

### `excel/` – Excel, wizualizacje i raporty  
- **`COVID-19.xlsx`** – dane w Excelu  
- **`EXCEL 1.jpg`** – pierwsza strona wizualizacji
- **`EXCEL 2.jpg`** – druga strona wizualizacji
  
---

## 📊 Opis danych  

- **Źródło**: World Health Organization (2025), przetworzone przez *Our World in Data*  
- **Zakres czasowy**: do 17 sierpnia 2025  
- **Jednostka**: przypadki  
- **Metodologia**:  
  - Dane tygodniowe zostały pobrane jako plik CSV/JSON/Excel.  
  - Na ich podstawie została dodana nowa tabela `daily-cases-estimated.csv`, w której liczba tygodniowych przypadków została podzielona przez 7 w celu oszacowania wartości dziennych.  

---

## 🔎 Analizy w tabeli `covid-19-cases`  

- 📍 **Najbardziej zakażone kontynenty** – agregacja przypadków na poziomie kontynentów  
- 🌍 **Ranking państw** – kraje o najwyższej liczbie przypadków  
- 🗺️ **Rozkład zakażeń** – procentowy udział poszczególnych regionów  
- 🧭 **Mapa zakażeń** – wizualizacja skupisk przypadków w ujęciu globalnym (heatmap / bubble map)  
- 📅 **Sumy zakażeń wg roku i miesiąca** – kolumna umożliwiająca analizę czasową (trend w ujęciu globalnym)  
- 💰 **Status ekonomiczny wg kontynentu** – dodatkowa kolumna klasyfikująca dane wg kategorii ekonomicznych (np. high-income, low-income)  
- 🌐 **Agregaty globalne** – sumy przypadków dla całego świata oraz wariant *„świat bez Chin”*  

