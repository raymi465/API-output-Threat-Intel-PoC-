# API-output-Threat-Intel-PoC
proof of concept of all api outputs

## Intro
Dit zijn de Proof of Concepts van alle API's van de oplossingen die mij het beste lijken.
Met deze PoC's probeer ik te zien welke van deze oplossingen de "beste" en meest extensieve output geeft voor wat er gevraagd wordt qua prijs.

Naast een toeligting van de PoC ga ik het ook hebben over de kosten en of de API key de prijs waard is.

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

## PoC
Binnen de PoC wordt er gezocht op het IP-adress 51.89.153.112.

Voor de PoC'swordt er gebruik gemaakt van de gratis versie van de API, dit kan betekenen dat sommige functionaliteiten niet uitgetest kunnen worden.

### IPVOID
De API van de oplossing IPVOID geeft in eerste instancie een Raw output, zonder enige opmaak.
In het document [IPVOID.json](IPVOID.json) is de json versie te zien van de output van de API.

In het document IPVOID.json is te zien dat er een lijst is van blacklists.
Binnen deze blacklist lijst is te zien of het IP-adres aangetroven wordt binnen de indiviuele blacklists, dit staat dan onder het kopje "detected".

Na de blacklists wordt er algemene informatie over het IP-adres verteld, zoals "reverse DNS", landnaam, stads naam, isp en asn.

Na de lijst van algemene informatie is er een kopje met anonymity, daaronder vallen of het een proxy is, een webproxy is, een VPN is, of het iets aan het hosten is en of het een tor is.

Hierna komt de risico score, hierin is te vinden hoe zeker de API is of het IP-adres een risico is of niet.

### AlienVault OTX
De API van de oplossing AlienVault OTX geeft in eerste instancie een Raw output, zonder enige opmaak.
In het document [AlienVault.json](Alienvault.json) is de json versie te zien van de output van de API.

Binnen de output van de Alienvault OTX API zijn verschillende pulses te zien, dit zijn paginas gerelateerd aan het IP-adres, en binnen deze pulsen zijn wat tags te zien.

Met deze tags kan je zien waaraan het IP-adres gelinkt wordt, maar of de tags juist zijn kan ik helaas niet met zekerheid zeggen.

### ipdata
De API van de oplossing ipdata geeft meteen een output in json format.
In het document [ipdata.json](ipdata.json) is de json output van de API te zien.

Bovenaan in het document is wat algemene informatie te zien over het IP-adres zoals de stad waar het IP-adres zich in begeeft, het land waar het IP-adres zich in bevind, de asn en het domein van het IP-adres.

Daarna krijg je drie kopjes die ik persoonlijk minder belanrijk vind namelijk languages, currency en time_zone.

Daarna krijg je in mijn opinie het belangrijkste kopje namelijk Threat. Hierin is te zien wat het kan zijn, bijvoorbeeld een tor, een proxy, etc., of het een Threat is, of het een attacker is en een lijst van blocklists waarin het IP-adres te vinden is.

### AbuseIPDB
De API van de oplossing AbuseIPDB geeft in eerste instancie een Raw output, zonder enige opmaak.
Binnen de handleiding voor de API kan er met verschillende programeer talen de API aanroepen en laat het meteen de script zien die je kan gebruiken.
In het document [AbuseIPDB.json](AbuseIPDB.json) is de json output van de API te zien.

Bovenaan in de data krijg je de abuseConfidenceScore te zien, deze geeft aan hoe zeker de API is dat het IP-adres gebruikt wordt voor verkeerde doeleinden.

Daarna wat algemene informatie over het IP-adres en dan in het laatste stuk kan je zien hoevaak het IP-adres is gerapporteerd voor misbruik.

### Ipregistry
De API van de oplossing Ipregistry geeft in eerste instancie een Raw output, zonder enige opmaak.
In het document [Ipregistry.json](Ipregistry.json) is de json versie te zien van de output van de API.

Bovenin het document is te zien wat het IP-adres is, welke versie IP-adres er gebruikt wordt, de hostname van het IP-adres en eventueel de carrier.

Daarna krijg je het bedrijf te zien dat aan het Ip-adres is gekoppeld.

Daarna de connecties zoals asn, domein en organisatie.

Daarna is er informatie te zien over de valuta van het land waarin het IP-adres zich bevind.

Vervolgens krijg je informatie te zien over de locatie van het IP-adres zoals, het continent, het land en de stad waarin het IP-adres zich bevind.

Als volgt krijg je informatie te zien gerelateerd aan security zoals is het IP-adres een aanvaller, een proxy, een tor, een VPN en/of een threat is.

Tot slot krijg je informatie over de tijdszone van het land waarin het IP-adres zich bevind.

### Ipinfo
