Introduzione
Spiegare in poche parole scopo della nostra analisi (prendere spunto da file del dataset)

Parte 1 – Data Analysis
Analisi generale delle variabili del dataset: quali sono numeriche, quali categoriche, (per ognuna vedere max, min, media, sd,…), distribuzioni delle variabili
Scelta response variable -> TPY (motivare)
Plot delle variabili in funzione di TPY
Correlazioni tra le variabili quantitative
Similitudini tra variabili:
-MSA e URBAN: URBAN è già contenuto in MSA
-PRO e TAXEXEMPT già contenute in ORGSTR(ORGSTR in più ha anche un’altra categoria(governmental unit)
Missed values: solo per la variabile SQRFOOT, mancano 10 valori -> si decide di togliere quelle righe
Indipendenza: i dati del 2000 non sono indipendenti da quelli del 2001 -> consideriamo due dataset diversi
 
Parte 2 – Linear models / Gamma 
Linear:
Osservazioni:
-no differenze tra usare solo variabili numeriche o tutte(anche categoriche)
-provati un sacco di modelli con tante combinazioni diverse -> alla fine scegliere solo i modelli più significativi
- modello migliore si ottiene con logTPY – logSQRFOOT
NUMBED risulta essere la variabile più significativa(guardando i valori del p-value), ma consideriamo come importante anche SQRFOOT(risulta rilevante da Anova)
Analisi outliers:
fatto utilization rate per individuare outliers(TPY/NUMBED) ma, anche il modello migliora togliendo outliers, non possiamo considerare l’utilization rate come un’ulteriore variabile nel modello(chi lo userà non lo conosce a priori)-> vedere se riusciamo a ricavare outliers considerando solo NUMBED e SQRFOOT (ad es: tanti letti ma poco posto, pochi letti ma tanto posto)
->	Fare 3 modelli diversi con le tre classi(outliers bassi, altri, valori medi)?
Problema del modello Lineare:
Residual plots non va bene:  i residual seguono una normale ma troppo concentrata al centro, meglio trovare altro modello -> provare con glm gamma

Parte 3 - Trees

Parte 4 - GAMs

Conclusioni
