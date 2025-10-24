# Analiza Churnu i Kampanii

Projekt eksploracyjnej analizy danych przygotowany na podstawie rzeczywistego zestawu kampanii marketingowych i danych o klientach.  
Analiza została wykonana w **Pythonie (EDA)** oraz **Power BI (dashboard wizualny)**.

---

## Cel projektu

Na bazie załączonych danych i ich opisu należało przygotować **eksploracyjną analizę danych**,  
której celem było:

- znalezienie **zależności i wzorców** w danych dotyczących kampanii i klientów,  
- przedstawienie **wniosków i rekomendacji** dla przyszłych akcji sprzedażowych,  
- zaprezentowanie wyników w formie **czytelnego dashboardu** w Power BI.

---

## Zakres analizy

Analiza obejmuje dane o klientach, kampaniach i wynikach rezygnacji w latach **2005–2020**.  
Plik źródłowy zawierał m.in. następujące kolumny:

| Kolumna | Opis |
|----------|------|
| `MIESIAC_KAMPANII` | miesiąc kampanii |
| `TYP_KAMPANII` | sposób prowadzenia kampanii (`scored`, `campaign`, `campaign out`) |
| `DECYL` | poziom ryzyka rezygnacji z usługi |
| `CZY_CHURN` | czy klient zrezygnował z usługi |
| `CZY_RETENCJA` | czy klient odnowił umowę |
| `DATA_EOP`, `rok_eop`, `msc_eop` | data zakończenia kontraktu |
| `N` | liczba zdarzeń |
| `KAT` | kategoria klienta (`OK` / `NIE`) |

---

## Eksploracja i przetwarzanie danych (Python)

Analiza eksploracyjna została wykonana w notatniku **`EDA_Dataset202508.ipynb`**, obejmując:
- wstępne czyszczenie i opis danych,
- wyliczenie wskaźników churnu oraz agregacji wg lat i kampanii,
- analiza korelacji (`CZY_RETENCJA` ↔ `CZY_CHURN`, korelacja ≈ 0.59),
- przygotowanie danych wejściowych do Power BI.

Repozytorium zawiera kod w Pythonie umożliwiający replikację analizy.

---

## Dashboard Power BI

Interaktywny raport dostępny online:  
**[Zobacz dashboard Power BI](https://app.powerbi.com/view?r=eyJrIjoiNGM4YmFhNWYtMDRkZC00NzRjLWFjZGItOTliOTdjYThmYThiIiwidCI6ImEyMDEyMWI0LWMxYzctNDkwOS05NzQ4LTk0NjU0NDVkNDI1MSJ9)**  

### Główne elementy raportu:
1. **Karty metryk głównych**  
   - Ostatni churn (mies.)  
   - Średni churn  
   - Łączna liczba klientów  
   - Średni decyl (poziom ryzyka)

2. **Wskaźnik churnu wg decyla**  
   - Analiza poziomu ryzyka rezygnacji w różnych grupach klientów.

3. **Churn rate wg typu kampanii**  
   - Porównanie skuteczności kampanii marketingowych (`scored`, `campaign`, `campaign out`).

4. **Udział churnu wg kategorii klienta (KAT)**  
   - Struktura klientów aktywnych (`OK`) vs. nieaktywnych (`NIE`).

5. **Trend churnu w czasie (2005–2020)**  
   - Analiza zmian wskaźnika churnu w ujęciu rocznym.  
   - Wykres trendu z zaznaczeniem spadków i wzrostów.

6. **Liczba zdarzeń wg typu kampanii (N)**  
   - Pokazuje intensywność działań sprzedażowych i marketingowych w czasie.

Dashboard został zaprojektowany z myślą o czytelności i spójności kolorystycznej.  
Użyto motywu **ciemnoszarego z niebieskimi akcentami**.

---

## Technologie

- **Python (Pandas, NumPy, Matplotlib)** – przygotowanie danych i analiza EDA  
- **Power BI Desktop / Power BI Service** – wizualizacja i dashboard  
- **GitHub** – wersjonowanie kodu i dokumentacja projektu

---

## Struktura repozytorium
```
Zadanie_rekrutacyjne_2/
│
├── Data
    └── churn_by_DECYL.csv
    └── churn_by_KAT.csv
    └── churn_by_TYPE.csv
    └── churn_trend.csv
    └── sample.csv
├── notebook
    └── EDA_Dataset202508.ipynb        # Analiza danych w Pythonie (EDA)
├── README.md                  # Opis projektu (ten plik)
└── .DS_Store
```

---

## Wnioski

- Największy churn odnotowano w latach **2015–2017**, z maksimum w 2016 r.  
- Kampanie typu **scored** generowały wyższy churn niż kampanie standardowe.  
- Klienci w kategorii **NIE** stanowili ok. **38,5%** wszystkich rezygnacji.  
- Korelacja **CZY_RETENCJA** z **CZY_CHURN** = **0.59**, co sugeruje umiarkowaną zależność – klienci, którzy nie odnowili umowy, częściej odchodzili.  

---

## Autor

**Mateusz Wykowski**  
 Październik 2025  

---
