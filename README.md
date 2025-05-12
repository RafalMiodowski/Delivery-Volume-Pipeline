# Delivery Volume Pipeline

Projekt analityczny dotyczący przetwarzania, analizy i prognozowania wolumenów przesyłek z uwzględnieniem danych kalendarzowych, branżowych, pogodowych oraz danych prognozowanych przez klientów.

## Zakres projektu

Projekt obejmuje:

- analizę wolumenów przesyłek z perspektywy ostatniego pełnego tygodnia (sobota–piątek) oraz ostatniego zakończonego miesiąca względem analogicznych okresów roku poprzedniego,
- porównanie wolumenów dla różnych branż oraz par krajów (nadania i doręczenia),
- uwzględnienie różnic w strukturze kalendarza (dni robocze, weekendy, święta),
- predykcję wolumenów przesyłek dla poszczególnych kierunków w horyzoncie 6 miesięcy,
- opcjonalne wykorzystanie danych pogodowych i prognoz klientów w modelach predykcyjnych,
- możliwość automatycznego generowania raportów dla dowolnie wybranego dnia w formacie notebooka lub pliku Excel.

## Dane źródłowe

- `DimDates` – plik CSV z informacjami kalendarzowymi (rok, miesiąc, dzień tygodnia, weekendy, święta),
- `PostingVolumes` – plik Parquet z dziennymi wolumenami przesyłek w podziale na usługi i klientów (2020–2024),
- `X_ClientORDERS` – prognozy zamówień dziennych od jednego z klientów dla usługi APM (plik Excel),
- `Customer_Industry` – przypisanie klientów do branż (plik Excel),
- `Zadanie_Dane_Temperatura` – folder z plikami CSV zawierającymi dane pogodowe (temperatura i opady) dla Warszawy i Krakowa (2022–2024).

> W repozytorium umieszczono wyłącznie zanonimizowane lub przykładowe dane (fragmenty), bez danych rzeczywistych.

## 🛠 Technologie

- Python (pandas, numpy, seaborn, matplotlib, xgboost, scikit-learn)
- Google Colab

##  Wynik

Efektem pracy jest kompletny notebook analityczny zawierający:
- analizę danych historycznych,
- wizualizacje porównawcze,
- model predykcyjny wolumenów,
- eksport wyników do Excela,
- funkcje umożliwiające analizę z perspektywy dowolnej daty.
