# Algorytmy i złożoność obliczeniowa

Program umożliwia wczytywanie danych z pliku, sortowanie wybranym algorytmem, zapisywanie wyników oraz wykonywanie benchmarków dla różnych konfiguracji.

## Zaimplementowane algorytmy
 - **Insertion Sort** - sortowanie przez wstawianie
 - **Heap Sort** - sortowanie przez kopcowanie
 - **Shell Sort** - sortowanie shella z wyborem sekwencji
 - **Quick Sort** - sortowanie szybkie z wyborem pivota
 - **Drunk Student Sort** - sortowanie przez wstawianie z popełnianiem błędów, a następnie ich korekcją

## Tryby działania
Program działa w trzech trybach:

- `--file` – sortowanie danych z pliku  
- `--test` – generowanie danych i uruchamianie benchmarku  
- `--help` – wyświetlanie pomocy

# Tryb FILE
Sortowanie danych pobranych z pliku.

## Uruchamianie (Windows)
```bash
projekt1_aizo.exe --file <algorithm> <type> <inputFile> [outputFile] <algType>
```

### Argumenty

#### **`<algorithm>`** – wybór algorytmu:
- `0` – Insertion Sort  
- `1` – Heap Sort  
- `2` – Shell Sort  
- `3` – Quick Sort  
- `4` – Drunk Student Sort  

#### **`<type>`** – typ danych:
- `0` – int  
- `1` – float  
- `2` – double  

#### **`<inputFile>`**  
Plik z danymi wejściowymi.

#### **`[outputFile]`**  
Plik docelowy (opcjonalny). Jeśli podany – wynik zostanie zapisany.

#### **`<algType>`** – konfiguracja algorytmu:
- **Quick Sort (PIVOT)**  
  `0` – lewy  
  `1` – prawy  
  `2` – środkowy  
  `3` – losowy  

- **Shell Sort (GAP)**  
  `0` – n/2, n/8, ...  
  `1` – ciąg Knutha: 1, 4, 13, 40, ..., (3^k − 1) / 2  

- **Drunk Student (INTOXICATION)**  
  Format: `T<0.value>`  
  wartość 0–1 ustalana na podstawie liczby cyfr argumentu  *(np. `7` → 0.7, `42` → 0.42)*


# Tryb TEST (Benchmark)
Generowanie danych oraz wykonywanie pomiarów dla wybranych algorytmów.

## Uruchamianie (Windows)
```bash
projekt1_aizo.exe --test <algorithm> <type> <size> <sorting> <outputFile> <numbersFile> <algType>
```


### Argumenty

#### **`<algorithm>`** – wybór algorytmu
- `0` – Insertion  
- `1` – Heap  
- `2` – Shell  
- `3` – Quick  
- `4` – Drunk Student  

#### **`<type>`** – typ generowanych danych
- `0` – int  
- `1` – float  
- `2` – double  

#### **`<size>`**
Liczba generowanych elementów.

#### **`<sorting>`** – początkowy układ tablicy  
- `0` – losowy  
- `1` – niemalejący  
- `2` – nierosnący  
- `3` – niemalejący w 33%  
- `4` – niemalejący w 66%  

#### **`<outputFile>`**
Plik, w którym zapisane zostaną wyniki benchmarku.

#### **`<numbersFile>`**
Plik z posortowaną tablicą (`-` oznacza brak zapisu).

#### **`<algType>`** – jak w trybie FILE  












