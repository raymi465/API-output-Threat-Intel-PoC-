# API-output-Threat-Intel-PoC
proof of concept of all api outputs

## Intro
Dit zijn de Proof of Concepts van alle API's van de oplossingen die mij het beste lijken.
Met deze PoC's probeer ik te zien welke van deze oplossingen de "beste" en meest extensieve output geeft voor wat er gevraagd wordt qua prijs.

Naast een toeligting van de PoC gan ik het ook hebben over de kosten en of de API key de prijs waard is.

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
### IPVOID
De API van de oplossing IPVOID geeft in eerste instancie een Raw output, zonder enige opmaak.
In het document [IPVOID.json](IPVOID.json) is de json versie te zien van de output van de API.
Binnen de PoC wordt er gezocht naar het IP-adress 51.89.153.112.
