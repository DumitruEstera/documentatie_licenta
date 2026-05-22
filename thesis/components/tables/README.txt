Folosește acest folder pentru a stoca tabelele separate (în fișiere `.tex` distincte) și a le include în capitole cu:

    \input{components/tables/nume_tabel}

De exemplu, pentru un tabel mic, conținutul `nume_tabel.tex` ar putea arăta așa:

    \begin{center}
        \begin{tabular}{| l | c | r |}
            \hline
            Coloana 1 & Coloana 2 & Coloana 3 \\
            \hline
            Valoare A & 1.23      & X         \\
            Valoare B & 4.56      & Y         \\
            \hline
        \end{tabular}
        \captionof{table}{Descrierea tabelului}
        \label{tab:nume_tabel}
    \end{center}
