
# Potok Przetwarzania i Oczyszczania Sygnałów EEG

## Opis projektu
Projekt implementuje zaawansowany potok (pipeline) do przetwarzania surowych danych neurofizjologicznych (zapis EEG). Program automatycznie pobiera rzeczywiste dane medyczne z międzynarodowej bazy **PhysioNet** za pomocą biblioteki `MNE-Python`. Następnie dokonuje cyfrowego filtrowania sygnału (redukcja szumów za pomocą średniej kroczącej), generuje statystyki opisowe amplitudy fal mózgowych oraz tworzy zaawansowane wykresy porównawcze surowego i przefiltrowanego sygnału bioelektrycznego.

## Źródło danych
Dane są pobierane bezpośrednio z bazy **PhysioNet (EEG Motor Movement/Imagery Dataset)**. Program automatycznie łączy się z serwerem, pobiera plik binarny `.edf` dla wybranego pacjenta, ekstrahuje centralny kanał sygnału (np. `Fcza.`) i skaluje amplitudę do mikrowoltów (µV), umożliwiając pracę na realnym, chaotycznym zapisie aktywności mózgu.

## Instrukcja instalacji

1. Upewnij się, że posiadasz środowisko Python w wersji min. 3.8:
```bash
python --version
```

2. Pobierz repozytorium:
```bash
git clone [https://github.com/heligoland1984/eeg-pipeline-project](https://github.com/heligoland1984/eeg-pipeline-project)
```

3. Wejdź do katalogu:
```bash
cd eeg-pipeline-project
```

4. Zainstaluj wymagane pakiety (w tym bibliotekę mne do obsługi danych EEG):
```bash
pip install -r requirements.txt
```

5. Uruchom program:
```bash
python main.py
```
