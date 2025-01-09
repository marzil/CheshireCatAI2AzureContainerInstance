# Cheshire Cat AI e l'Integrazione con Azure Container Instance
Sono molti coloro che mi conoscono e sanno quanto sia stato un fervente sostenitore di Piero Savastano. Questo non è solo perché credo fermamente nel suo progetto, ma perché lo ritengo un esempio di eccellenza nel settore tecnologico, progettato con grande cura e competenza.


[Sito internet di Cheshire Cat AI](https://cheshirecat.ai/)

![Cheshire Cat AI Logo](https://cheshirecat.ai/wp-content/uploads/2023/10/Logo-Cheshire-Cat.svg)

Tuttavia, nonostante la solidità e il supporto della comunità, anche i progetti più raffinati possono incontrare ostacoli, specialmente quando si tratta di scalabilità aziendale e di sicurezza nel cloud. Queste sono sfide reali che richiedono soluzioni pratiche per garantire che il nostro lavoro possa prosperare e adattarsi ai rigori dell'ambiente aziendale moderno.

Per affrontare queste criticità, ho sviluppato una serie di script progettati per migliorare la sicurezza dell'infrastruttura. L'obiettivo è di rendere l'installazione di container Docker su Azure non solo accessibile, ma anche più sicura, anche per chi è alle prime armi. Questi strumenti permettono di inserire agevolmente i propri container all'interno di un'infrastruttura Azure robusta e sicura.

È importante notare che questo processo non è privo di difficoltà, specie considerando che Azure e Microsoft non forniscono un'assistenza diretta in questo ambito, se non tramite script altamente personalizzati. Tuttavia, troverete tutte le risorse necessarie in questo repository. La vostra collaborazione è fondamentale e sono più che aperto a ricevere suggerimenti per migliorare ulteriormente le procedure e l'architettura complessiva.

Auguro a tutti un buon lavoro e un'esperienza costruttiva nell'implementazione di queste soluzioni.

## Descrizione dell'Architettura

![Architecture](img/ArchitectureDiagram.png)

L'obiettivo del progetto è garantire un ambiente sicuro e controllato per l'interazione tra i servizi AI e le risorse aziendali. In particolare, desideriamo esporre le API del servizio Microsoft OpenAI esclusivamente all'interno della rete virtuale (VNet) di Azure, garantendo che il container Docker di Cheshire Cat AI operi solo all'interno di questa stessa VNet. Questo approccio assicura che le comunicazioni siano protette da accessi indesiderati, limitando le interazioni ai confini definiti della rete virtuale.

La macchina virtuale attualmente in uso funge da dimostrazione pratica, dimostrando che il sistema è accessibile solo internamente alla rete. Tuttavia, in una fase successiva, questa configurazione può essere ulteriormente ottimizzata. La macchina virtuale potrebbe essere rimossa a favore di una segmentazione della VNet, collegandola tramite una VPN dedicata per una connessione sicura con altre reti. In alternativa, si potrebbe sviluppare un Gateway tramite una WebApp, permettendo al sistema di comunicare in modo sicuro verso l'esterno.

Inoltre, per chi desidera un livello ancora più sofisticato di gestione e sicurezza delle API, esiste l'opzione di integrare Azure API Management. Questo servizio altamente affidabile permette non solo di orchestrare e proteggere le API, ma anche di monitorarle e scalarle in modo efficiente. Utilizzando Azure API Management, è possibile costruire un'architettura che non solo assicura sicurezza e prestazioni, ma che offre anche un controllo dettagliato sulle modalità di accesso e utilizzo delle API.

In sintesi, il nostro approccio flessibile e lungimirante offre una struttura che può evolvere in funzione delle esigenze future, garantendo sempre il massimo livello di sicurezza e operatività.
