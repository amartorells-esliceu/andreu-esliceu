# Gestió del Sistema Operatiu:
La gestió del sistema operatiu és un aspecte crític per al funcionament eficient i coordinat d'un sistema informàtic. Implica una sèrie de funcionalitats que asseguren que els recursos del sistema es distribueixin i utilitzin de manera òptima per satisfer les demandes dels programes i usuaris. Aquí hi ha alguns dels elements clau que formen part de la gestió del sistema operatiu:
## Creació de processos:
- Quan s'inicia un programa, el sistema operatiu crea un procés associat.
- La creació implica la inicialització d'una estructura de dades anomenada Bloc de Control de Procés (PCB) que emmagatzema informació vital com l'estat del procés, el seu comptador de programa, i els recursos assignats.
## Assignació de recursos:
- El sistema operatiu és responsable de gestionar els recursos del sistema, incloent-hi la CPU, la memòria i els dispositius d'entrada/sortida.
- Cada procés rep una porció del temps de CPU i la quantitat necessària de memòria, garantint que els recursos siguin compartits de manera equitativa.
## Control de canvis d'estat:
- Els processos poden passar per diversos estats com ara "llest", "en execució", "bloquejat" o "acabat".
- La gestió del sistema operatiu controla aquestes transicions per garantir una execució ordenada dels processos.
## Planificació de Processos:
- El sistema operatiu utilitza algoritmes de planificació per decidir quin procés s'executarà a la CPU en un moment determinat.
- Algoritmes com FIFO, Round Robin, SJF, i altres determinen l'ordre d'execució dels processos.
## Gestió de Memòria:
- Assegura la correcta assignació i alliberament de blocs de memòria als processos.
- Prevé la fragmentació de la memòria per optimitzar l'ús eficient d'aquest recurs.
## Gestió de Dispositius:
- Supervisa i coordina l'accés als dispositius d'entrada/sortida per part dels processos.
## Suspensió i Reanudació de Processos:
- El sistema operatiu pot suspendre temporalment un procés per alliberar recursos, i posteriorment reprendre la seva execució.
## Terminació de Processos:
- Quan un procés ha completat la seva tasca, el sistema operatiu l'atura i allibera els recursos associats.
## Gestió d'Errors i Excepcions:
- Tracta situacions inesperades com errors de programari o excepcions hardware per mantenir la integritat del sistema.
## Gestió de Fitxers i Estructures de Dades:
- Proporciona funcionalitats per gestionar l'accés als fitxers i organitzar les dades emmagatzemades al sistema.