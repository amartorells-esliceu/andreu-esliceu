# Planificadors:
## FIFO (First In, First Out):
Els processos s'executen en l'ordre en què entren a la cua. És senzill però pot generar un problema d'"injustícia" si processos més curts han d'esperar que processos més llargs acabin.
## Round Robin:
Cada procés rep un interval de temps de CPU (quantum) i es canvia al següent procés quan s'esgota el temps. Evita el problema d'"injustícia", però pot haver-hi una sobrecàrrega de canvi de context.
## SJF (Shortest Job First):
Els processos s'executen segons la durada més curta. Pot minimitzar el temps d'espera, però pot haver-hi problemes de predicció.
## SRT (Shortest Remaining Time):
Similar al SJF, però la CPU es pot canviar si apareix un procés amb un temps d'execució més curt que el procés en execució.
## Prioritats:
Els processos s'executen segons la prioritat assignada. Pot ser preemptiu (el sistema operatiu pot canviar l'execució) o no preemptiu (el procés conserva la CPU fins que acaba o es bloqueja).