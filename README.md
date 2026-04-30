# DAVIDEMATTEO_HACKATHONML

Hackathon Machine Learning -
Previsione Abbandono Universitario
Tempo a disposizione: 8 ore (2 laboratori)
Il Contesto Aziendale:
Siete stati contattati da una grande università che ha un problema urgente: troppi
studenti abbandonano gli studi prima della laurea, causando sia un danno
d'immagine che una perdita economica per l'ateneo. L'università vuole intervenire
proattivamente contattando gli studenti a rischio prima che decidano di
abbandonare.
Hanno raccolto i dati di iscrizione e i risultati del primo anno accademico di circa
3.000 studenti. Il vostro compito è costruire un modello di Machine Learning capace
di prevedere in anticipo chi si laureerà ("Graduate") e chi abbandonerà ("Dropout").
Per info sulle colonne, potete consultare il dataset qui:
https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-stude
nt-retention
Il lavoro va svolto a coppie.
I Dati a Disposizione:
Avete ricevuto due file:
1. train_dropout.csv: Contiene 2904 record storici con tutte le variabili, compresa
la colonna Target (Dropout o Graduate). Usate questo file per fare
esplorazione (EDA) e addestrare il vostro modello.
2. test_dropout.csv: Contiene 726 nuovi studenti di cui non conoscete l'esito.
Sono i nuovi iscritti dell'anno in corso!
L'Obiettivo (L'Hackathon):
Alla fine delle due lezioni dovrete consegnare un file CSV contenente esattamente
726 righe con le vostre previsioni (Dropout o Graduate) corrispondenti agli studenti
del file di test. Il cliente (l'università) non vuole un modello che dica solo chi si laurea.
Vuole scovare chi abbandona. Per questo vincerà chi ha l'F1-score Macro più alto,
perché questa metrica penalizza chi indovina solo la maggioranza. In base alle
vostre performance, verrà stilata una classifica e saranno assegnati i seguenti premi:
● Jolly Hackathon – Premio 1° classificato
Ogni studente della coppia vincitrice ottiene 1 jolly che rende corretta
automaticamente una domanda a scelta del test teorico.
● Jolly Hackathon – Premio 2° classificato
Ogni studente della coppia seconda classificata ottiene 1 jolly “50/50” su una
domanda a scelta del test teorico. Su quella domanda il docente elimina
un'alternativa errata, lasciando solo due opzioni possibili.
Come Lavorare (Suggerimenti del Cliente):
● Non fidatevi ciecamente dei dati grezzi. Il modello migliore non sarà quello
dell'algoritmo più complesso, ma quello di chi saprà interrogare meglio i dati
(Feature Engineering).
● Hint per una nuova feature: Un ragazzo che passa dal superare 5 esami nel
primo semestre a superarne 1 nel secondo è a rischio? Come potete spiegare
matematicamente questa cosa al modello?
● Provate a pensare quali features potrebbero essere utili per la vostra
predizione, e arricchite il vostro dataset!
● Lavorate a coppie: in due si pensa meglio.
Cosa dovete consegnare:
1. Il Jupyter Notebook pulito e commentato con tutto il processo (EDA,
preprocessing, feature engineering e training).
2. Il file CSV con le vostre predizioni finali. Usate questo codice per produrle:
predizioni = model.predict(X_test)
submission = pd.DataFrame({'Target': predizioni})
submission.to_csv('my_submission.csv', index=False)
3.
4. Preparatevi a spiegare al "Rettore dell'Università" (il docente) perché il vostro
modello funziona e quali sono le 3 variabili più importanti che determinano
l'abbandono degli studi.
Buon lavoro :)