# Estats d'un Procés:
- Ready:
  En aquest estat, el procés està preparat per ser executat i ha estat carregat a la memòria. No està utilitzant actualment la CPU, però està disponible per ser programat.
- Run:
  En aquest estat, el procés té accés a la CPU i està executant les seves instruccions. Només un procés pot estar en aquest estat a la vegada per cada unitat de processador.
- Wait:
  Quan un procés espera per algun esdeveniment (com ara entrada/sortida o una resposta a una crida de sistema), entra en l'estat bloquejat. Durant aquest temps, no utilitza la CPU i allibera recursos.
  ![ESQUEMA DE ESTAT DE PROCESSOS](PROCESSOS.png)

- Això és la [intruduccio](01_Introduccio.md)
- Això son els meus apunts de [gestió de sistemes](<02_Gestió del Sistema Operatiu.md>)
- Això son els meus apunts de [execució de processos](<03_Execució de Processos.md>)
- Això son els meus apunts de [operacions amb processos](<04_Operacions amb Processos.md>)
- Això son els meus apunts de [planificadors](06_Planificadors.md)

- Gràcies per haver llegit els meus apunts, fes [clic aqui](.) per tornar a la carpeta de processos