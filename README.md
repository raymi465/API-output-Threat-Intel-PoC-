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


