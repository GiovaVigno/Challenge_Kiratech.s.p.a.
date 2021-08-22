**API** (acronimo di Application Programming Interface, ovvero Interfaccia di programmazione delle applicazioni) 

Sono degli strumenti di programmazione che vengono messi a disposizione degli sviluppatori per facilitare il loro compito nella realizzazione di applicazioni di vario genere e permettono una semplice interazione con servizi informatici messi a disposizione da altri (es. da delle banche, aziende di servizi, IT company...).

**API SOAP**: (Simple Object Access Protocol) definisce una struttura dati per lo scambio

di messaggi tra applicazioni, riproponendo in un certo senso parte di quello che il protocollo

HTTP già faceva;

**API REST** sono indipendenti dai linguaggi o da precise piattaforme. Si sanno adattare sempre e in ogni occasione, garantendo quindi la massima libertà. Puoi avere un server PHP, Java, Python o Node.js senza riscontrare alcun problema; la separazione client-server si traduce in una migliore scalabilità del sistema stesso;

**AVS (**Address Verification System**)** 

È il servizio che conta sul supporto di Visa, Mastercard, Discover e American Express

che consente di verificare l’indirizzo di fatturazione del titolare della carta con quello

registrato nel database dell’issuer

**ATO (account takeover)** 
si fa riferimento alla pratica fraudolenta

**IBAN:**

prevedendo:

\- una lettera per il CIN: Control Internal Number, è utilizzato come carattere di controllo.

\- 5 numeri per l'ABI: rappresenta l'istituto di credito, assegnato dall’ABI (Associazione Bancaria Italiana)

\- 5 numeri per il CAB: Codice di Avviamento Bancario, è un numero composto da cinque cifre e rappresenta l'agenzia o specifica filiale dell'istituto di credito identificato dal codice ABI

\- 12 caratteri (alfanumerici) per il conto corrente per fare un bonifico

**DCC:** dynamic currency conversion

**Interoperabilità**: utilizzo dello standard ISO 20022

**Payment Gateways**

È la tecnologia (un SaaS) che consente la trasmissione delle informazioni relative ad una transazione per le banche acquirenti e le risposte dalle banche emittenti. Il payment gateway raccoglie le informazioni necessarie per processare il pagamento, tramite messaggi cryptati, vengono gestiti ed inviati agli acquirer di riferimento

• Authorising: verifica dei dettagli della carta del compratore;

• Clearing: Trasferimento della transazione alla banca merchant;

• Reporting – registrazione di tutte le transazioni;

**Clearing and settlement** tra il cliente che dispone il pagamento e la sua banca e (ii) tra la banca destinataria e il cliente beneficiario).

In questa fase si realizza la compensazione (clearing: trasmissione, riconciliazione, conferma dei pagamenti e determinazione di una posizione finale per il regolamento) e il regolamento (settlement: estinzione delle obbligazioni determinate nel clearing) dei flussi di pagamento, secondo il c.d. modello dei “CSM” (Clearing and Settlement Mechanism), costituito da uno o più soggetti che svolgono congiuntamente le funzioni di compensazione e di regolamento

**PCI DSS (Payment Card Industry Data Security Standard)**

È l’insieme di requisiti e standard a cui devono sottostare

**PSD2**

L’obiettivo della “Services Directive 2 – PSD2” è standardizzare le modalità di esecuzione dei pagamenti digitali, per rendere più sicure le transazioni e tutelare i consumatori

**SET**

Questo sistema di sicurezza fu progettato da Visa e Mastercard per le transazioni tramite carta di credito.

Il SET introduce due nuove entità:

• la certification authority, che certifica i partecipanti;

• il payment gateway, che fa da filtro tra Internet e la rete bancaria.

Il SET garantisce la sicurezza degli scambi sia tra cliente e commerciante che tra il commerciante ed il gateway.

**SSL (Security Sockets Layer)**

Permette uno scambio cifrato dei dati tra client e server. Ormai quasi tutti i browser supportano il protocollo SSL; in Google Chrome ad esempio appare un lucchetto chiuso accanto al link del sito per indicare la connessione a un sito sicuro via SSL.

**Issuer:** l’emittente della Carta di Credito

**Acquirer:** Banca dell’esercente che gestisce la transazione in fase autorizzativa.

**Merchant:** l’esercizio commerciale convenzionato al circuito di pagament

**Circuito di Pagamento**: è la società interbancaria che ha il compito di trasferire mediante il proprio network informativo

**Tokenizzazione**

È il servizio che permette di archiviare, su server sicuri del Payment Gateway, i dati delle carte dei propri clienti permettendo di chiudere le operazioni di acquisto in un solo click (come operano ad esempio i grandi application store on line). Utile anche in caso di pagamenti ricorrenti come gli abbonamenti.

Vantaggi

\- Risparmio di costi

\- Maggiore sicurezza

\- Abilitazione pagamenti 0 click

Il sistema di tokenization applica al **PAN** (primary account number) un algoritmo di criptatura

**Interchange fee**

Interchange fee è una commissione che viene pagata tra le banche per l’accettazione delle

transazioni con carta di pagamento. Per l’acquirer IRF fee è un costo da pagare alla banca Issuer quando gestisce la transazione per un merchant.

Le Interchange Fee o Commissioni Interbancarie sono quelle che gli Issuer e gli Acquirer si

scambiano a fronte di un’operazione di pagamento o di prelievo

**Merchant Fee**

Quando un consumatore acquista un bene o un servizio con una carta di debito o credito, la

banca che ha convenzionato l'esercente (ossia la banca Acquirer) addebita una commissione a quest'ultimo - la c.d. Merchant Fee - il cui valore include quello dell‘Interchange Fee. Un processo fino a oggi invisibile all'acquirente, che in alcuni casi può subire inconsapevolmente il ricarico della fee sul prezzo finale (EUP End User Price).

