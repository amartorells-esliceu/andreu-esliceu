# Planificadors:
## FIFO (First In, First Out):
L'algoritme de planificació FIFO segueix el principi simple de "el primer que arriba és el primer que surt". Quan un nou procés arriba a la cua de planificació, es col·loca al final de la cua, i el procés que està a la part frontal de la cua és el que obté l'oportunitat de ser executat següent.
### Característiques destacades:
1. **Senzillesa:**
   - El major avantatge de l'algoritme FIFO és la seva simplicitat. La implementació és directa i fàcil de comprendre.
2. **Implementació de Cua:**
   - La cua de processos es manté mitjançant una estructura de dades tipus cua, on els processos s'afegeixen a la part posterior i s'eliminen de la part frontal.
3. **Problema d'"Injustícia":**
   - Malgrat la seva simplicitat, el principal inconvenient de FIFO és el problema d'"injustícia". Si un procés llarg arriba a la cua abans que un procés curt, aquest últim ha de esperar fins que els processos més llargs finalitzin.
4. **No Óptim per Temps d'Espera:**
   - FIFO no és òptim per minimitzar els temps d'espera dels processos. Processos curts poden veure's afectats per temps d'espera excessius a causa de processos més llargs que els precedeixen.
### Exemple d'Execució:
Suposem que tenim tres processos en aquest ordre a la cua: P1, P2 i P3. Si arriben amb els temps d'execució de 5, 10 i 3 unitats de temps, respectivament, l'execució podria ser la següent:
1. **Temps 0:**
   - P1 arriba i comença a executar-se.
2. **Temps 5:**
   - P1 finalitza i P2 comença a executar-se.
3. **Temps 15:**
   - P2 finalitza i P3 comença a executar-se.
### Limitacions:
- **Problema de "Injustícia":**
  - El principal inconvenient de FIFO és que no té en compte la durada dels processos. Això pot portar a situacions on processos més curts han de esperar innecessàriament a causa de processos més llargs.
- **No Óptim en Temps d'Espera:**
  - Els temps d'espera poden ser elevats, especialment per a processos curts en presència de processos llargs.
- **No Dinàmic:**
## Round Robin:
L'algoritme de planificació Round Robin és una millora del FIFO que aborda el problema d'"injustícia". Cada procés rep un interval de temps de CPU conegut com a "quantum", i s'executa durant aquest temps. Si no ha finalitzat, es mou al final de la cua, permetent als altres processos ser executats. Aquest model de planificació és àgil, però pot provocar una sobrecàrrega de canvis de context.
### Característiques destacades:
1. **Quantum de Temps:**
   - El "quantum" determina el temps que cada procés pot ocupar la CPU abans de ser interromput per donar pas al següent procés.
2. **Abordatge d'"Injustícia":**
   - Round Robin evita el problema d'"injustícia" assegurant que tots els processos tinguin l'oportunitat d'executar-se en intervals iguals.
3. **Sobrecàrrega de Canvis de Context:**
   - Tot i ser just, l'ús excessiu de canvis de context pot generar una sobrecàrrega, especialment amb "quants" petits.
4. **Implementació de Cua Circular:**
   - Round Robin s'implementa amb una cua circular, on els processos es mouen davanter cap enrere.
### Exemple d'Execució:
Suposem tres processos (P1, P2 i P3) amb "quants" de temps de CPU de 8 unitats. L'execució podria ser:
1. **Temps 0-8:**
   - P1 executa 8 unitats.
2. **Temps 8-16:**
   - P2 executa 8 unitats.
3. **Temps 16-24:**
   - P3 executa 8 unitats.
4. **Temps 24-32:**
   - P1 executa 8 unitats, i així successivament.
### Limitacions:
- **Sobrecàrrega de Canvis de Context:**
  - "Quants" petits poden provocar una sobrecàrrega en els canvis de context, ja que els processos es commuten amb freqüència.
- **No Óptim per Temps d'Espera:**
  - Encara pot generar temps d'espera significatius per a processos curts si hi ha molts processos llargs a la cua.
## SJF (Shortest Job First):
L'algoritme de planificació SJF (Shortest Job First) busca minimitzar el temps d'espera prioritzant els processos amb la durada més curta. Tot i les seves avantatges, la seva implementació pràctica pot ser desafiadora a causa de la necessitat de predir la durada dels processos amb antelació.
### Característiques destacades:
1. **Minimització del Temps d'Espera:**
   - SJF té la capacitat de minimitzar el temps d'espera total prioritzant l'execució dels processos més curts.
2. **Problemes de Predicció:**
   - La principal desavantatge és la necessitat de conèixer la durada dels processos abans de l'execució, el que pot ser difícil de predir amb precisió.
### Exemple d'Execució:
Suposem tres processos (P1, P2 i P3) amb temps d'execució de 6, 8 i 4 unitats, respectivament. L'execució podria ser:
1. **Temps 0-4:**
   - P3 executa 4 unitats.
2. **Temps 4-12:**
   - P1 executa 6 unitats.
3. **Temps 12-20:**
   - P2 executa 8 unitats.
### Limitacions:
- **Problemes de Predicció:**
  - La predicció precisa de la durada dels processos és crucial per a l'eficàcia de SJF.
- **Potenciales Temps d'Espera Elevats:**
  - Si un procés més llarg arriba abans que un més curt, aquest últim haurà d'esperar fins que finalitzi el procés llarg.
## SRT (Shortest Remaining Time):
SRT (Shortest Remaining Time) és una variant dinàmica de SJF, on la CPU pot ser canviada a un nou procés si aquest té un temps d'execució més curt que el procés en execució actual. Aquesta característica dinàmica pot reduir encara més els temps d'espera.
### Característiques destacades:
1. **Dinamisme:**
   - La CPU pot ser commutada a un nou procés si aquest té un temps d'execució més curt que el procés actual.
2. **Reducció de Temps d'Espera:**
   - SRT busca minimitzar els temps d'espera i adaptar-se a canvis dinàmics en la càrrega del sistema.
### Exemple d'Execució:
Suposem dos processos (P1 i P2) amb temps d'execució de 6 i 8 unitats, respectivament. L'execució podria ser:
1. **Temps 0-6:**
   - P1 executa 6 unitats.
2. **Temps 6-8:**
   - P2 arriba i té un temps d'execució més curt que el que queda per a P1, així que la CPU es commuta a P2.
3. **Temps 8-16:**
   - P2 executa 8 unitats.
### Limitacions:
- **Canvis de Context Addicionals:**
  - La dinàmica de canvis en el procés actual pot provocar canvis de context addicionals, que podrien afectar el rendiment en certes situacions.
- **Complexitat de Implementació:**
  - La implementació de SRT pot ser més complexa que altres algoritmes a causa de la necessitat de supervisar els temps d'execució restants de manera dinàmica.