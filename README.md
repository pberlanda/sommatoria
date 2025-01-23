L'esempio è stato tratto dal libro di testo Syntax (pag. 437). Nel programma originale, c'è un bug. 
Il button del form determina il refresh della pagina, quindi non si vede il risultato del calcolo.
Bisogna impedire il refresh, e di conseguenza gestire anche lo svuotamente del campo importo per prepararlo a una nuova immissione.
Ho trovato due metodi, entrambi presenti nel codice

metodo civile (intercetto l'evento del btn, e con questa istruzione impedisco il comportamento previsto, cioè il refresh)
if (event) event.preventDefault();

metodo selvaggio (da aggiungere come ultima istruzione, in pratica sto dicendo che il programma non funziona e lo blocco, impedendo il refresh che sarebbe il prossimo evento)
return 1;

Inoltre negli input type text bisogna imporre l'attributo value="0" altrimenti la somma non funziona (input vuoto viene considerato da javascript come "")
