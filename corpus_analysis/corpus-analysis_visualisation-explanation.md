(corpus-analysis_visualisation)=
# Analyse und Visualisierung
## Quantitative Analyse 
Nachdem wir verschiedene Textkomplexitätsmaße kennengelernt haben, geht es in diesem Abschnitt um die diachrone Analyse der Textkomplexität der Pressemitteilungen. Ziel ist es, festzustellen, ob die Komplexität über Zeit zu- oder abnimmt. Dafür haben wir die Komplexität für jede Pressemitteilung berechnet und dann über Zeit akkumuliert. Die Akkumulierung kann über unterschiedlich große Zeitabschnitte ausgeführt werden. Da selten mehrere Pressemitteilungen an einem Tag veröffentlicht werden, ergibt es Sinn als kleinste Zeiteinheit eine Woche festzulegen. Da unser Korpus mehrere Jahre umfasst, können wir zusätzlich Monate und Jahre als Zeiteinheiten festlegen. 
Für jede Zeiteinheit wird der Durchschnitt der Textkomplexitätsmaße errechnet. Dieser kann dann mit den vorherigen und folgenden verglichen werden.

% Verteilungen der Pressemitteilungen hier 

## Visualisierung
Um die Werte besser vergleichen zu können, bietet es sich an, diese visuell darzustellen. In einem Liniendiagramm, in dem die X-Achse in die Zeiteinheiten eingeteilt ist und die Y-Achse die Textkomplexität darstellt, werden zunächst alle Datenpunkte eingetragen und dann zu einer Linie verbunden. Da anhand der Linie lokale und globale Minima sowie Maxima gut erkennbar werden und sich leicht ein Trend ablesen lässt, eignet sich das Liniendiagramm gut zur Darstellung einer zeitlichen Entwicklung. 
Die Häufigkeiten über Zeit ließen sich auch in einem Balkendiagramm darstellen. Diese sind nützlich, um Häufigkeiten in diskreten Zeitintervallen zu visualisieren, sie eignen sich aber weniger gut, um eine zeitliche Entwicklung zu zeigen. 
