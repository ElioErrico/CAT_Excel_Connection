# Cheshire Cat Excel Add-in

Add-in per Excel che integra la funzionalità di chat con Cheshire Cat AI direttamente nei fogli di calcolo.

## Installazione

1. **Scarica il file .xlam** dalla repository
2. **Posiziona il file** in una delle seguenti cartelle:
   - `C:\Users\[TuoiUtente]\AppData\Roaming\Microsoft\AddIns\`
   - `C:\Program Files (x86)\Microsoft Office\Root\OfficeXX\Library\`
  
## Configurazione

Modifica le credenziali nel codice VBA (se necessario):
```vba
Private Const DEFAULT_URL As String = "http://localhost:1865"
Private Const DEFAULT_USERNAME As String = "admin"
Private Const DEFAULT_PASSWORD As String = "admin"
```
## Configurazione
Apri Excel

  Vai su:
  - File → Opzioni → Componenti aggiuntivi
  - In "Gestisci", seleziona Componenti aggiuntivi Excel e clicca Vai...
  - Clicca Sfoglia e seleziona il file .xlam
  - Assicurati che la checkbox sia selezionata
  - Clicca OK

## Utilizzo nei Fogli

In qualsiasi cella Excel, inserisci la formula:

    =CheshireCat_Chat("Il tuo messaggio")
    =CheshireCat_classify("sentence";[list of cells])

Opzioni avanzate:

    Mantenere cronologia: =CheshireCat_Chat("Messaggio", 0)

    Cancellare cronologia: =CheshireCat_Chat("Messaggio", 1) (default)

