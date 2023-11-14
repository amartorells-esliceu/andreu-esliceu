# Execució de Processos:
La execució de processos és una fase crucial de la gestió del sistema operatiu, ja que implica la transformació del codi d'un programa en instruccions executables per la CPU. Aquí tens més detalls sobre aquesta etapa:
1. **Creació de Processos:**
   - Abans de l'execució, cal crear un procés associat al programa que es vol executar. Aquesta creació implica la reserva d'espai de memòria per al procés i la inicialització del seu PCB amb informació crítica.
2. **Càrrega de Programes:**
   - El codi del programa és carregat des del sistema d'emmagatzematge a la memòria principal. Aquesta càrrega pot implicar la resolució d'adreces, la configuració de punters i la preparació del codi per a l'execució.
3. **Inicialització del PCB:**
   - El Bloc de Control de Procés (PCB) emmagatzema informació com l'estat del procés, el comptador de programa, els registres i altres detalls crucials. La inicialització d'aquesta estructura és essencial abans de l'execució.
4. **Planificació del Processador:**
   - Abans d'executar el procés, el sistema operatiu decideix si és el moment adequat per donar-li accés a la CPU. Això depèn de l'algoritme de planificació i de l'estat actual del sistema.
5. **Execució de Processos:**
   - Un cop obtingut l'accés a la CPU, el processador comença a executar les instruccions del programa contingudes a la memòria.
   - El PCB manté el registre de l'estat actual del procés, com ara els registres del processador, l'estat de la memòria i l'adreça de la propera instrucció.
6. **Control de Interrupcions i Excepcions:**
   - Durant l'execució, es poden produir interrupcions (eventualment procedents d'entrada/sortida) o excepcions (errors o condicions inesperades). El sistema operatiu ha de gestionar aquestes situacions de manera adequada.
7. **Planificació Prèvia o No Preemptiva:**
   - En sistemes amb planificació no preemptiva, el procés manté la CPU fins que finalitza o es bloqueja. En sistemes preemptius, el sistema operatiu pot prendre la decisió d'aturar l'execució del procés i donar l'oportunitat a un altre.
8. **Gestió de Prioritats:**
   - En sistemes on es fa servir la planificació per prioritats, els processos s'executen segons la seva prioritat assignada. Això pot ser crucial per donar preferència a certs processos segons les necessitats del sistema.
9. **Finalització del Procés:**
   - Quan el procés ha completat la seva tasca, el sistema operatiu realitza les accions necessàries per alliberar els recursos associats. Això pot incloure la lliberació de memòria, la finalització del PCB i altres tasques de neteja.
10. **Comunicació Interprocessos:**
    - En sistemes on diversos processos necessiten comunicar-se, s'utilitzen mecanismes com les cues, els semàfors o les pipes per intercanviar informació.

    - Gràcies per haver llegit els meus apunts, fes [clic aqui](.) per tornar a la carpeta de processos