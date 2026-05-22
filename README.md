# Lucrare de Licență – Soluție inteligentă de analiză a înregistrărilor video

Schelet LaTeX pentru lucrarea de licență a lui **Dumitru Estera**, construit peste șablonul [iosifache/Thesis-Diploma-Templates](https://github.com/iosifache/Thesis-Diploma-Templates) (Academia Tehnică Militară „Ferdinand I" București, Facultatea de Sisteme Informatice și Securitate Cibernetică).

Fiecare capitol există ca fișier `.tex` separat, populat doar cu titlul capitolului și ierarhia de secțiuni/subsecțiuni. Conținutul propriu-zis se adaugă manual.

## Structura proiectului

```
thesis/
├── main.tex                                # Punct de intrare LaTeX
├── main.sty                                # Pachet de stil (nu modifica)
├── configuration.tex                       # Detalii personale (titlu, autor, coordonator)
├── bibliography.bib                        # Surse bibliografice (BibTeX)
└── components/
    ├── frontmatter/
    │   ├── all.tex                         # Agregator front matter
    │   ├── title.tex                       # Prima pagină
    │   ├── acknowledgment.tex              # Mulțumiri
    │   ├── adviser_resume.tex              # Referatul coordonatorului
    │   ├── specification.tex               # Tema proiectului
    │   ├── abstract.tex                    # Rezumat / Abstract
    │   └── abbreviations.tex               # Listă de abrevieri
    ├── chapters/
    │   ├── all.tex                         # Agregator capitole
    │   ├── introducere.tex                 # Cap. 1
    │   ├── stadiul_actual.tex              # Cap. 2
    │   ├── fundamente_teoretice.tex        # Cap. 3
    │   ├── analiza_si_proiectare.tex       # Cap. 4
    │   ├── implementare_ai.tex             # Cap. 5
    │   ├── implementare_web.tex            # Cap. 6
    │   ├── testare_evaluare.tex            # Cap. 7
    │   ├── concluzii.tex                   # Cap. 8
    │   └── bibliography.tex                # Bibliografia (afișare)
    ├── images/
    │   └── ATM.png                         # PLACEHOLDER – înlocuiește cu sigla ATM
    └── tables/                             # Tabele separate (opțional)
```

## Pași pentru a începe redactarea

1. **Importă arhiva în Overleaf**: New Project → Upload Project → ZIP-ul.
2. **Înlocuiește `components/images/ATM.png`** cu sigla oficială a Academiei Tehnice Militare (din șablonul original).
3. **Completează `configuration.tex`** cu:
   - Specializarea ta exactă (înlocuiește textul gri din `\setdetailspecialization`).
   - Gradul + numele complet al coordonatorului științific.
   - Verifică gradul tău în `\setdetailauthor`.
4. **Redactează capitolele** unul câte unul, în fișierele `.tex` din `components/chapters/`. Structura de secțiuni este deja pregătită.
5. **Adaugă surse bibliografice** în `bibliography.bib`. Folosește [Google Scholar](https://scholar.google.com/) pentru a obține citări BibTeX, apoi citează-le din text cu `\cite{cheie}`.
6. **Compilează** cu pdfLaTeX + Biber (Overleaf face acest lucru automat).

## Setări speciale făcute în acest schelet

- `secnumdepth = 4` și `tocdepth = 4` în `frontmatter/all.tex` → permite numerotarea și apariția în Cuprins a nivelelor de tip `\paragraph` (necesare în Cap. 5 pentru sub-sub-subsecțiunile datasetului de vandalism: 5.6.2.3.1, 5.6.2.3.2, etc.).
- Toate capitolele folosesc `\subfile{...}` (modul `subfiles`), deci poți compila individual fiecare fișier dacă vrei să iterezi mai repede pe un singur capitol.
- Lista de abrevieri (`abbreviations.tex`) e pre-populată cu termenii principali ai proiectului (AI, API, CNN, FAISS, FPS, GPU, HSV, IoU, JWT, mAP, OCR, ONNX, RBAC, REST, YOLO). Adaugă/șterge după nevoie.

## Ce trebuie să mai faci înainte de predare

- Completează `acknowledgment.tex` (Mulțumiri).
- Completează `abstract.tex` (rezumat în română + abstract în engleză), după ce termini conținutul.
- Coordonatorul completează `adviser_resume.tex` și (eventual) `specification.tex`.
- Dacă specializarea ta nu impune partea de inventariere a lucrării, comentează `\showinventary` în `configuration.tex`.

## Resurse utile (din README-ul șablonului original)

- [Overleaf](https://www.overleaf.com/project) – platforma LaTeX online recomandată.
- [Google Scholar](https://scholar.google.com/) – căutare surse + export BibTeX.
- [LucidChart](https://www.lucidchart.com/) / [StarUML](https://staruml.io/) – pentru diagrame UML din Cap. 4.
- [LanguageTool](https://languagetool.org/) – verificare gramaticală a textului.
- [dexonline](https://dexonline.ro/) – definiții pentru limba română.
- [Lagrida LaTeX Editor](https://latexeditor.lagrida.com/) – construire vizuală de ecuații.

## Notă despre conținut

Acest schelet conține **doar** structura capitolelor și a secțiunilor. Toate `\chapter{...}`, `\section{...}`, `\subsection{...}`, `\subsubsection{...}` și `\paragraph{...}` sunt poziționate conform Cuprinsului propus, dar fără text între ele. Adaugă textul direct între aceste comenzi, în fișierele corespunzătoare.
