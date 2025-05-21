---
connections:
  - "[[Sistemi e Reti]]"
source:
  - Pag. 310 - 337
  - Powerpoint
---

Un amministratore di rete deve mantenere efficiente la rete. Le attività che svolge sono di due tipi:
- host configuration: ogni host dev'essere configurato prima del suo utilizzo e della messa in rete, per svolgere il suo compito al meglio;
- host management: la gestione e il controllo degli host da remoto in modo tale da rilevare anomalie e cali di prestazione;

Il principale protocollo usato per la configurazione degli host è il DHCP (Dynamic Host Configuration Protocol). Per la gestione della rete si usa invece il protocollo SNMP (Simple Network  Management Protocol). 
> Entrambi appartengono al livello Application

---

# Il DHCP

Quando nelle reti si diffusero la tecnologia wireless e l’uso di computer portatili, in ambito IETF fu definito il protocollo DHCP (Dynamic Host Configuration Protocol), la cui specifica si trova in RFC 2131.

Tramite DHCP, oltre all’indirizzo IP, un host può ricevere altri parametri di configurazione: 
- subnet mask
- default gateway: per esempio l’indirizzo IP del router che connette la subnet alla rete Internet. A questo sono inviati i pacchetti IP aventi indirizzo di rete del destinatario diverso da quello del mittente;
• DNS Server preferito;
• DNS Server alternativo;

---

*Assegnazione degli Indirizzi*
DHCP usa il MAC Address per identificare l'host. Il server utilizza questo dato e il network address della rete a cui l'host è connesso, per consultare il database e stabilire se assegnare all'host un indirizzo IP permanente o temporaneo. Ogni volta che un host si connette a una rete, il suo DHCP Client richiede un indirizzo IP al DHCP Server, che lo sceglierà tra quelli nell'address pool.

---
*Configurazione Modalità*
L’amministratore di rete può configurare, per ogni subnet e per ogni host, la modalità con cui il DHCP Server risponderà alle richieste dei client scegliendo fra 3 diversi tipi di configurazione.

- Configurazione manuale: è possibile assegnare un indirizzo IP specifico a un host, inserendolo manualmente nel DHCP Server; di regola si utilizza per macchine come router e server che si trovano stabilmente in una rete o per host che necessitano di un indirizzo permanente;
- Configurazione automatica: il DHCP Server assegna in modo automatico un indirizzo IP permanente a ogni host che si collega alla rete (si differenzia dalla configurazione dinamica per l’assenza del tempo di lease);
- Configurazione dinamica: il DHCP Server assegna un indirizzo IP a un host per un tempo limitato (tempo di lease) in base alla lease length policy stabilita. Allo scadere del tempo di lease il client può richiederne il rinnovo o richiedere l’assegnazione di un nuovo indirizzo;

---

*L'Architettura Client Server DHCP*
Un solo DHCP Server è solitamente in grado di soddisfare le esigenze operative relative all’assegnazione degli indirizzi IP e al setting dei parametri di configurazione sui client della rete locale. In condizioni normali il carico che deriva da queste attività non è particolarmente pesante. 

Un DHCP Server può anche essere configurato per servire più subnet, per due scopi:
- fault-tolerance: per cui in genere è opportuno inserire un secondo DHCP Server come backup, così da mantenere il servizio sempre attivo;
- bilanciamento del carico di lavoro: così da diminuire i tempi di risposta del server. In tal caso, alla richiesta di un client per l’assegnazione di un indirizzo IP possono rispondere più di un DHCP Server;

Quando un DHCP Server è responsabile dell’indirizzamento su una subnet diversa dalla propria è necessario introdurre un relay agent (agente di ritrasmissione), ossia una macchina che non è né un server né un client, ma svolge un ruolo di intermediario occupandosi di facilitare la comunicazione tra client e server attraverso più reti.

---

*La Comunicazione tra DHCP Client e DHCP Server*
I messaggi di trasporto tra DHCP Client e DHCP Server sono di due tipi: richieste (request) e risposte (reply). Il protocollo di trasporto utilizzato è UDP e utilizza le porte 67 per il server e 68 per il client.

---

*Il Pacchetto DHCP*
- op (operation code)
- htype (hardware type)
-  hlen (Hardware address length)
-  hops (Hops count)
- Transaction ID (xid)
- Seconds (secs)
- Flags (flags)
- Client IP address (ciaddr)
- ‘Your’ (client) IP address (yiaddr)
- Server IP address (siaddr)
- Gateway IP address (giaddr)
- Client hardware address (chaddr)
- Server host name (sname)
- Boot file name (file)
- Options;

---

*Problematiche di Sicurezza*
Il DHCP utilizza i protocolli UDP e IP che sono intrinsecamente insicuri. Sono due i principali problemi di sicurezza:
- DHCP Server non autorizzati: un DHCP Server abusivo potrebbe inserirsi e inibire gli host o configurarli per azioni fraudolente; 
- DHCP Client non autorizzati: un host potrebbe danneggiare la rete, oppure esaurire gli indirizzi a disposizione e bloccare nuovi accessi;

Per ovviare al problema si possono implementare meccanismi di sicurezza ai livelli più bassi, inoltre si potrebbe usare IPsec per rendere sicuro il livello Network.

---

# DNS

