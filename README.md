# Analiza Churnu i Kampanii

Projekt analizy rezygnacji klientów (churn) w kontekście kampanii marketingowych, wykonany w **Pythonie (EDA)** oraz **Power BI (wizualizacja wyników)**.

---

## Cel projektu

Celem projektu było:
- zidentyfikowanie trendów odejść klientów (churn),
- analiza wpływu typu kampanii oraz kategorii klientów na poziom churnu,
- wizualizacja kluczowych wskaźników w postaci przejrzystego dashboardu w Power BI.

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

Analiza eksploracyjna została wykonana w notatniku **`Zadanie_rekrutacyjne2.ipynb`**, obejmując:
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
1. **Karty metryk** – ostatni churn, średni churn, liczba klientów, średni decyl.  
2. **Wskaźnik churnu wg decyla** – analiza ryzyka rezygnacji w różnych grupach klientów.  
3. **Churn rate wg typu kampanii** – porównanie skuteczności kampanii (`scored`, `campaign`, `campaign out`).  
4. **Udział churnu wg kategorii klienta (OK/NIE)** – analiza struktury rezygnacji.  
5. **Trend churnu w czasie (2005–2020)** – wizualizacja dynamiki odejść klientów.  
6. **Liczba zdarzeń wg typu kampanii (N)** – wolumen działań marketingowych.  

Dashboard został zaprojektowany z myślą o czytelności i spójności kolorystycznej.  
Użyto motywu **ciemnoszarego z niebieskimi akcentami**.

---

## Technologie

- **Python (Pandas, NumPy, Matplotlib)** – przygotowanie danych i analiza EDA  
- **Power BI Desktop / Power BI Service** – wizualizacja i dashboard  
- **GitHub** – wersjonowanie kodu i dokumentacja projektu

---

## 🧾 Struktura repozytorium
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

##� Wnioski

- Największy churn odnotowano w latach **2015–2017**, z maksimum w 2016 r.  
- Kampanie typu **scored** generowały wyższy churn niż kampanie standardowe.  
- Klienci w kategorii **NIE** stanowili ok. **38,5%** wszystkich rezygnacji.  
- Korelacja **CZY_RETENCJA** z **CZY_CHURN** = **0.59**, co sugeruje umiarkowaną zależność – klienci, którzy nie odnowili umowy, częściej odchodzili.  

---

## Autor

**Mateusz Wykowski**  
💼 Data Analyst / Data Science Enthusiast  
📅 Październik 2025  

---
