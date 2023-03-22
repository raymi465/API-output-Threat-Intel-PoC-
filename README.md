# API-output-Threat-Intel-PoC
proof of concept of all api outputs

## Intro
Dit zijn de Proof of Concepts van alle API's van de oplossingen die mij het beste lijken.
Met deze PoC's probeer ik te zien welke van deze oplossingen de "beste" en meest extensieve output geeft voor wat er gevraagd wordt qua prijs.

Naast een toeligting van de PoC ga ik het ook hebben over de kosten.

---
## Inhoudsopgaven
- [API-output-Threat-Intel-PoC](#API-output-Threat-Intel-PoC)
  - [Intro](#Intro)
  - [PoC](#PoC)
    - [IPVOID](#IPVOID)
    - [AlienVault OTX](#AlienVault-OTX)
    - [ipdata](#ipdata)
    - [AbuseIPDB](#AbuseIPDB)
    - [Ipregistry](#Ipregistry)
    - [Ipinfo](#Ipinfo)
  - [Kosten](#Kosten)
    - [IPVOID](#IPVOID)
    - [AbuseIPDB](#AbuseIPDB)
    - [Ipregistry](#Ipregistry)
    - [ipdata](#ipdata)
    - [IP Adress.ipynb/ msticpy](#IP-Adress.ipynb/-msticpy)
    - [Ipinfo](#Ipinfo)
    - [native solution](#native-solution)
    - [AlienVault OTX](#AlienVault-OTX)
    - [IPsum](#IPsum)
    - [Ip_enrich](#Ip_enrich)

---
## PoC
Binnen de PoC wordt er gezocht op het IP-adress 51.89.153.112.

Voor de PoC'swordt er gebruik gemaakt van de gratis versie van de API, dit kan betekenen dat sommige functionaliteiten niet uitgetest kunnen worden.

### IPVOID
De API van de oplossing IPVOID geeft in eerste instancie een Raw output, zonder enige opmaak.
In het document [IPVOID.json](IPVOID/IPVOID_51.89.153.112.json) is de json versie te zien van de output van de API.

In het document IPVOID.json is te zien dat er een lijst is van blacklists.
Binnen deze blacklist lijst is te zien of het IP-adres aangetroven wordt binnen de indiviuele blacklists, dit staat dan onder het kopje "detected".

Na de blacklists wordt er algemene informatie over het IP-adres verteld, zoals "reverse DNS", landnaam, stads naam, isp en asn.

Na de lijst van algemene informatie is er een kopje met anonymity, daaronder vallen of het een proxy is, een webproxy is, een VPN is, of het iets aan het hosten is en of het een tor is.

Hierna komt de risico score, hierin is te vinden hoe zeker de API is of het IP-adres een risico is of niet.

### AlienVault OTX
De API van de oplossing AlienVault OTX geeft in eerste instancie een Raw output, zonder enige opmaak.
In het document [AlienVault.json](AlienVault/Alienvault_51.89.153.112.json) is de json versie te zien van de output van de API.

Binnen de output van de Alienvault OTX API zijn verschillende pulses te zien, dit zijn paginas gerelateerd aan het IP-adres, en binnen deze pulsen zijn wat tags te zien.

Met deze tags kan je zien waaraan het IP-adres gelinkt wordt, maar of de tags juist zijn kan ik helaas niet met zekerheid zeggen.

### ipdata
De API van de oplossing ipdata geeft meteen een output in json format.
In het document [ipdata.json](ipdata/ipdata_51.89.153.112.json) is de json output van de API te zien.

Bovenaan in het document is wat algemene informatie te zien over het IP-adres zoals de stad waar het IP-adres zich in begeeft, het land waar het IP-adres zich in bevind, de asn en het domein van het IP-adres.

Daarna krijg je drie kopjes die ik persoonlijk minder belanrijk vind namelijk languages, currency en time_zone.

Daarna krijg je in mijn opinie het belangrijkste kopje namelijk Threat. Hierin is te zien wat het kan zijn, bijvoorbeeld een tor, een proxy, etc., of het een Threat is, of het een attacker is en een lijst van blocklists waarin het IP-adres te vinden is.

### AbuseIPDB
De API van de oplossing AbuseIPDB geeft in eerste instancie een Raw output, zonder enige opmaak.
Binnen de handleiding voor de API kan er met verschillende programeer talen de API aanroepen en laat het meteen de script zien die je kan gebruiken.
In het document [AbuseIPDB.json](AbuseIPDB/AbuseIPDB_51.89.153.112.json) is de json output van de API te zien.

Bovenaan in de data krijg je de abuseConfidenceScore te zien, deze geeft aan hoe zeker de API is dat het IP-adres gebruikt wordt voor verkeerde doeleinden.

Daarna wat algemene informatie over het IP-adres en dan in het laatste stuk kan je zien hoevaak het IP-adres is gerapporteerd voor misbruik.

### Ipregistry
De API van de oplossing Ipregistry geeft in eerste instancie een Raw output, zonder enige opmaak.
In het document [Ipregistry.json](Ipregistry/Ipregistry_51.89.153.112.json) is de json versie te zien van de output van de API.

Bovenin het document is te zien wat het IP-adres is, welke versie IP-adres er gebruikt wordt, de hostname van het IP-adres en eventueel de carrier.

Daarna krijg je het bedrijf te zien dat aan het Ip-adres is gekoppeld.

Daarna de connecties zoals asn, domein en organisatie.

Daarna is er informatie te zien over de valuta van het land waarin het IP-adres zich bevind.

Vervolgens krijg je informatie te zien over de locatie van het IP-adres zoals, het continent, het land en de stad waarin het IP-adres zich bevind.

Als volgt krijg je informatie te zien gerelateerd aan security zoals is het IP-adres een aanvaller, een proxy, een tor, een VPN en/of een threat is.

Tot slot krijg je informatie over de tijdszone van het land waarin het IP-adres zich bevind.

### Ipinfo
De API van de oplossing Ipinfo geeft meteen een output in json format.
In het document [Ipinfo_gratis.json](Ipinfo/Ipinfo_gratis_51.89.153.112.json) is de json output van de API te zien van een gratis account.
En in het document [Ipinfo.json](Ipinfo/Ipinfo_51.89.153.112.json) is de json output van de API te zien van de verschillende accounts, met boven elk stukje een comment over welk profiel nodig is voor de daaronder geleverde informatie.

Bovenin het documetn Ipinfo_gratis.json is het IP-adres te zien met daaronder de hostname van het IP-adres.

Daarna is er wat informatie over de locatie van het IP-adres te zien zoals stad, land en regio.

Vervolgens krijg je wat informatie over de organisatie te zien.

Tot slot krijg je wat informatie over de tijdszone.


Bovenin het document Ipinfo.json is de algemene informatie te zien die ook al zijn benoemd in het Ipinfo_gratis.json bestand.

Daarna krijg je informatie over de ASN van het IP-adres.

Vervolgens krijg je informatie over het achterliggende bedrijf.

Als volgt krijg je informatie over privacy gerelateerde zaken zoals is het een VPN verbinding, is het een tor node en is het iets aan het hosten.

Daarna krijg je informatie te zien over het melden van misbruik van het IP-adres zoals wat is de e-mail adres die je kan mailen voor het melden van misbruik.

Tot slot is er informatie te zien gerelateerd aan het domain van het IP-adres.

---
## Kosten
Binnen dit kopje geef ik aan wat de verschillende betaal manieren zijn binnen de oplossing en de kosten van de verschillende profielen als deze aanwezig zijn.

### IPVOID
- 0.08 credits per query, credits zijn een jaar geldig, voor een custom plan kunnen ze gecontacteerd worden
  - 1000 credits voor 12 USD
  - 2500 credits voor 25 USD
  - 5000 credits voor 45 USD
  - 10000 credits voor 80 USD
  - 25000 credits voor 180 USD
  - 50000 credits voor 300 USD
  - 100000 credits voor 500 USD
  - 250000 credits voor 1000 USD
  - 500000 credits voor 1700 USD
  - 1000000 credits voor 3000 USD

### AbuseIPDB
- maandelijkse en jaarlijkse opties
  - Gratis: 
    - 1000 IP checks & rapporten per dag
    - 100 prefix checks per dag
    - een basis blacklist tot 10000 IPs
  - Basic: Jaarlijks $19 per maand of maandelijks $25 per maand:
    - 10000 IP checks & rapporten per dag
    - 1000 prefix checks per dag
    - een basis blacklist tot 100000 IPs
    - 5 traceerbare prefixen
  - Premium: Jaarlijks $89 per maand of maandelijks $99 per maand:
    - 50000 IP checks & rapporten per dag
    - 5000 prefix checks per dag
    - een basis blacklist tot 500000 IPs
    - 25 traceerbare prefixen
    - prioriteiten support – 24 uur per dag
  - Contact opnemen voor de enterprise opties

### ipregistry
- Elke lookup kost een credit 
  - 40000 credits voor 5 USD
  - 100000 credits voor 10 USD
  - 700000 credits voor 50 USD
  - 2000000 credits voor 100 USD
  - 11000000 credits voor 500 USD
  - Enterprise oplossing: neem contact op met sales voor de opties.

### ipdata
- maandelijkse en jaarlijkse opties
  - Personal: Jaarlijks $96 per jaar of maandelijks $10 per maand: 
    - 2500 verzoeken per dag
    - geolocatie data
    - IP blocklijsten
    - ASN data.
  - Lite: Jaarlijks $288 per jaar of maandelijks $30 per maand:
    - 10000 verzoeken per dag
    - geolocatie data
    - IP blocklijsten
    - ASN data.
  - Startup: Jaarlijks $480 per jaar of maandelijks $50 per maand: 
    - 50000 verzoeken per dag
    - geolocatie data
    - IP blocklijsten
    - ASN data 
    - bedrijfsdata.
  - Business: Jaarlijks $1152 per jaar of maandelijks $120 per maand:
    - 2500 verzoeken per dag
    - geolocatie data
    - IP blocklijsten
    - ASN data
    - Bedrijfsdata
    - VPN detector 
    - IP reputatie scores.
  - Enterprice, contact opnemen met sales:
    - hoge volume verzoeken korting
    - 99.999% uptime SLA
    - data downloads
    - custom datasets 
    - support SLA.

### IP Adress.ipynb/ msticpy
- is een notebook aangeboden door Azure-sentinel.
- Wel moeten de volgende API’s aangeschaft worden:
  - vrustotal premium API key
    - ergens tussen de $XX.000 en de $XXX.000
  - alienvault
    - bij het aanmaken van een account krijg je meteen toegang tot de API
  - IBM Xforce
    - lijkt erop dat je toegang krijgt tot de API als je een account hebt

### ipinfo
- maandelijkse en jaarlijkse opties
  - Basic: Jaarlijks $990 per jaar/$83 per maand of maandelijks $99 per maand: 
    - 150000 verzoeken per maand
    - $20 per 10000 extra verzoeken
    - geolocatie data
    - ASN data 
    - basis support.
  - Standard: Jaarlijks $2490 per jaar/$208 per maand of maandelijks $249 per maand:
    - 250000 verzoeken per maand
    - $30 per 25000 extra verzoeken
    - geolocatie data
    - ASN data
    - privacy detective waaronder vpn en  tor 
    - prioriteit support.
  - Business: Jaarlijks $4990 per jaar/$416 per maand of maandelijks $499 per maand: 
    - 500000 verzoeken per maand
    - $60 per 50000 extra verzoeken
    - abuse data
    - ISP data
    - achter liggende bedrijven
    - gehosten domeinen 
    - prioriteit support.
  - custom, contact opnemen met sales: 
    - flexibele hoeveelheid verzoeken per maand
    - IP whois data
    - IP ranges
    - IP activiteiten
    - support SLA
    - account manager 
    - onboarding.

### native solution
- de API van vrustotal moet aangeschaft worden.
  - ergens tussen de $XX.000 en de $XXX.000
- mogelijk nog overige kosten.

### AlienVault OTX
- gratis

### IPsum
- gratis

### Ip_enrich
- Wel moeten de volgende API’s aangeschaft worden:
  - virustotal premium API key
    - ergens tussen de $XX.000 en de $XXX.000
  - PassiveTotal
    - een gratis versie
    - een enterprice versie, kosten onbekend
