Probabilità stimata (0<Pa<1) di vittoria del giocatore A

$$
P_a = \frac{1}{1 + 10^{\frac{R_b - R_a}{500}}}
$$

Pa=1/(1+10^((Rb-Ra)/500)
dove 
- Ra = rating giocatore A (lo stesso)
- Rb = rating giocatore B (l'avversario)

la stessa per il giocatore B 

ora per calcolare il nuovo rating  

Nuovo rating per A = vecchio rating A + K*(Sa - Pa)
 dove
 - Pa è calcolato
 - Sa è invece lo score ottenuto (0 per sconfitta e 1 per vittoria, non è contemplato il pareggio
 - K è una costante variabile per il numero di game giocati (copiata dai game online)

$$
K_a = \frac{50}{1 + \left( \frac{N_a}{300} \right)}
$$

Ka = 50/(1+(Na/300))

dove Na è il numero di partite giocate

Per il 2 v 2 Pa diventa la media tra le due probabilità stimata dei singoli giocatori (quindi contro avversario uno C e contro avversario 2 D)

$$
P_a = \left( \frac{1}{1 + 10^{\frac{R_c - R_a}{500}}} + \frac{1}{1 + 10^{\frac{R_d - R_a}{500}}} \right) / 2
$$

Pa=((1/(1+10^((Rc-Ra)/500))+(1/(1+10^((Rd-Ra)/500)))/2

ripetere per ogni giocatore del match

A questo punto calcolare la probabilità di vincita del Team come la media delle singole probabilità

T1=(Pa+Pb)/2

a questo punto per calcolare il nuovo rating dopo una partita 

nuovo rating giocatore A = Vecchio rating giocatore A + k*(T1 - Pa)

REGOLE AGGIUNTIVE

è possibile aggiungere una variabile per considerare anche la differenza punti (copiata anche questa)

$$
D = 2 + \left( \log_{10} \left( | \text{score team 1} - \text{score team 2} | + 1 \right) \right)^3
$$

D = 2 + (log10(|score team 1 - score team2| + 1))^3

la formula finale diventa così

nuovo rating giocatore A = Vecchio rating giocatore A + (Ka*P)*(T1 - Pa)
 


