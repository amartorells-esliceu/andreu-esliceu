# Execució de Processos:
## Creació de processos:
Abans de l'execució, cal crear un procés associat al programa que es vol executar. Aquesta creació implica la reserva d'espai de memòria per al procés i la inicialització del seu PCB amb informació crítica.
## Càrrega de programes:
El codi del programa és carregat des del sistema d'emmagatzematge a la memòria principal. Aquesta càrrega pot implicar la resolució d'adreces, la configuració de punters i la preparació del codi per a l'execució.
## Execució de processos:
- Un cop obtingut l'accés a la CPU, el processador comença a executar les instruccions del programa contingudes a la memòria.
- El PCB manté el registre de l'estat actual del procés, com ara els registres del processador, l'estat de la memòria i l'adreça de la propera instrucció.