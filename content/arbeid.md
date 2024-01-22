---
title: Arbeid
---

## SAFEST-prosjektet

Siden august 2021 har jeg jobbet på SAFEST-prosjektet hos *Direktoratet for medisinske produkter (DMP)* (tidligere *Statens Legemiddelverk*[^1]). Formålet med prosjektet var opprinnelig å etablere en kilde til strukturert legemiddelinformasjon som understøtter behovene i sykehus. Men i en rapport fra *Helsedirektoratet* (tidligere *Direktoratet for e-helse*[^2]) som skulle vurdere den strategiske retningen for en kilde til felles legemiddelgrunndata, blir SAFEST-prosjektet trukket frem som en viktig del av målarkitekturen og den strategiske retningen for felles legemiddelgrunndata[^3].

### Bakgrunn

Mye av bakgrunnen for dette prosjektet er behovet for å gå over til internasjonale standarder, som er avgjørende for et effektivt leverandørmarked og internasjonal samhandling. Norge er ganske tidlig ute med dette, noe som blir lagt merke til [utenfor landegrensene](#key-innovator).

Grunnen til at SAFEST-prosjektet blir trukket frem av *Helsedirektoratet* er på bakgrunn av hva dataen som leveres i prosjektet kan tilby. Målarkitekturen de legger frem beskriver følgende forhold rundt en nasjonal tjeneste:

1. **Felles informasjonsmodell** for legemiddelgrunndata basert på ISO IDMP og felles informasjonsmodell for deling i verdikjeden basert på ressurser i FHIR.
2. **Standardiserte og åpne grensesnitt** for utveksling og distribusjon av legemiddelgrunndata skjer med API'er basert på FHIR.
3. **Teknisk løsning** som legger til rette for effektiv sentral informasjonsforvaltning og utveksling av data fra ulike produsenter og til konsumenter. Løsningene fra SAFEST-prosjektet kan ligge til grunn for komponenter i en teknisk løsning.
4. **Definerte roller og ansvar** der produsenter, konsumenter og integrator inngår i
leveranse og forvaltningskjeden for grunndata, og en **overordnet koordinering av behov og tiltak**.

Det blir også trukket frem i rapporten at helsesektoren i Norge i all hovedsak støtter dette forslaget til målarkitetur og et ønske om å gå i denne retningen.

### Key Innovator

SAFEST-prosjektet er med på å understøtte implementering og utbredelse av en felles standard på medisinske produkter og det er derfor Norge har blitt trukket frem av EU-kommisjonens «Innovation Radar» som en «Key Innovator»[^4].

### Teknisk implementasjon

I all hovedsak består den tekniske løsningen av 4 hovedkomponenter.

- **Dataoverføringsmodulen** betjenes hostes i Microsoft Azure.
- **Kvalitetsforbedringsmodulen**, med transformasjon til FHIR-format og -struktur, betjenes av pipelines i [Sesam](https://www.sesam.io/).
- **Kvalitetskontrollprosessene** håndteres gjennom GUI i Microsoft Dynamics 365.
- **Distribusjonsmodulen** hostes i Microsoft Azure.

![tekniske-platformer](/tekniske-platformer.png)

Det har også blitt utviklet et omfattende test-rammeverk for å validere


[^1]: [Praktisk informasjon: overgangen til nytt direktorat](https://www.dmp.no/nyheter/praktisk-informasjon-om-overgangen-til-nytt-direktorat).
[^2]: [Praktisk informasjon om endringene fra 1. januar 2024 på e-helseområdet](https://www.ehelse.no/aktuelt/endringer-pa-e-helseomradet-fra-1.januar-2024).
[^3]: [Strategisk retning for felles legemiddelgrunndata](https://www.ehelse.no/publikasjoner/strategisk-retning-for-felles-legemiddelgrunndata/).
[^4]: [Norge får EU-skryt for arbeid med legemiddelinformasjon](https://www.dagensmedisin.no/legemidler-spesialisthelsetjeneste/norge-far-eu-skryt-for-arbeid-med-legemiddelinformasjon/104110).