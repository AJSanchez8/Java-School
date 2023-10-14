# Code.Makery - Imparare a programmare

[Iscriviti agli Aggiornamenti](link_to_subscription)

## Home
- [Libreria](#library)
- [Percorsi](#paths)
- [Blog](#blog)
- [Su di Noi](#about)

## Articoli in questa Serie
- [Introduzione](#introduzione)
- [Parte 1: Scene Builder](#parte-1-scene-builder)
- [Parte 2: Modello e TableView](#parte-2-modelo-e-tableview)
- [Parte 3: Interazione con l'Utente](#parte-3-interazione-con-lutente)
- [Parte 4: Stili CSS](#parte-4-stili-css)
- [Parte 5: Persistenza dei Dati con XML](#parte-5-persistenza-dei-dati-con-xml)
- [Parte 6: Grafici Statistici](#parte-6-grafici-statistici)
- [Parte 7: Distribuzione](#parte-7-distribuzione)

## Tutorial JavaFX (Italiano)
### Parte 1: Scene Builder

Data: 17 Settembre 2014

![Screenshot AddressApp Parte 1](screenshot_link)

#### Contenuti nella Parte 1
- Conoscenza di JavaFX
- Creazione e Avvio di un Progetto JavaFX
- Utilizzo di Scene Builder per Progettare l'Interfaccia Utente
- Struttura di Base di un'Applicazione Utilizzando il Pattern Model-View-Controller (MVC)

#### Prerequisiti
- Ultima versione di Java JDK 8 (include JavaFX 8).
- Eclipse 4.3 o superiore con il plugin e(fx)clipse. Il modo più semplice per ottenerlo è scaricare la distribuzione preconfigurata dal [sito web di e(fx)clipse](https://efxclipse.bestsolution.at/install.html#all-in-one). In alternativa, puoi utilizzare un sito di aggiornamento per la tua installazione di Eclipse.
- Scene Builder 2.0 o superiore

#### Configurazione di Eclipse
- Apri le Preferenze di Eclipse (menu Finestra | Preferenze) e vai a Java | JRE Installate.
- Se non hai jre1.8 nell'elenco delle JRE, clicca su Aggiungi..., seleziona VM Standard e scegli la directory di installazione del JDK 8 (Directory Home JRE).
- Rimuovi altre JRE o JDK in modo che il JDK 8 diventi l'opzione predefinita.
- Vai su Java | Compilatore. Imposta il livello di conformità del compilatore su 1.8.
- Vai su Java | JavaFX. Specifica il percorso del file eseguibile di Scene Builder.

#### Collegamenti Utili
- [API di Java 8](https://docs.oracle.com/javase/8/docs/api/) - Documentazione (JavaDoc) delle classi standard di Java
- [API di JavaFX 8](https://docs.oracle.com/javase/8/javafx/api/) - Documentazione delle classi JavaFX
- [Tutorial JavaFX di Oracle](https://docs.oracle.com/javase/8/javafx/get-started-tutorial/get_start_apps.htm) - Tutorial ufficiali di Oracle su JavaFX

Ora, cominciamo!

#### Crea un Nuovo Progetto JavaFX
- In Eclipse (con e(fx)clipse installato), vai su File | Nuovo | Altro... e seleziona Progetto JavaFX. Specifica il nome del progetto (ad esempio, AddressApp) e clicca su Fine.
- Elimina il package dell'applicazione e il suo contenuto se è stato creato automaticamente.

#### Crea i Package
- Fin dall'inizio, seguiremo i buoni principi di progettazione del software. Alcuni di questi principi si traducono nell'uso dell'architettura nota come Model-View-Controller (MVC). Questa architettura promuove la divisione del codice in tre parti chiaramente definite, una per ciascun elemento dell'architettura. In Java, questa separazione si ottiene creando tre package separati.
- Fai clic con il pulsante destro del mouse sulla cartella src, quindi seleziona Nuovo | Package:
  - ch.makery.address - conterrà la maggior parte delle classi di controllo (C)
  - ch.makery.address.model - conterrà le classi del modello (M)
  - ch.makery.address.view - conterrà le viste (V)
  - Nota: Il nostro package dedicato alle viste conterrà anche alcuni controller dedicati esclusivamente a una vista. Li chiameremo controller di vista.

#### Crea il File di Progettazione FXML
- Ci sono due modi per creare l'interfaccia utente: programmala in Java o utilizza un file XML. Puoi trovare informazioni su entrambi i met
