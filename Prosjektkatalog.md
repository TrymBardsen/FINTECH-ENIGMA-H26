# Prosjektkatalog – Fintech Enigma Analysegruppe, høsten 2026

## Generell informasjon

Prosjektene er laget for grupper på omtrent 2–6 studenter og bør normalt kunne gjennomføres over 6–10 uker ved siden av studiene.

En god standardleveranse kan være:

- GitHub-repository med dokumentert kode
- Analyserapport eller en kortere «research note»
- Kort presentasjon
- Eventuelt dashboard/nettside
- Kort refleksjon rundt hva som faktisk kan og ikke kan konkluderes fra analysen

## 1. Kan teknisk analyse faktisk slå markedet?

**Passer for:** 1.–4. kull  
**Gruppestørrelse:** 3–5  
**Tema:** Backtesting, teknisk analyse, statistikk og programmering

### Prosjektidé

Teknisk analyse er svært populært blant både private investorer og profesjonelle tradere, men det er langt fra åpenbart at indikatorer som glidende gjennomsnitt, RSI og MACD faktisk inneholder informasjon som kan brukes til å oppnå risikojustert meravkastning.

Gruppen skal bygge et enkelt rammeverk for backtesting og undersøke dette empirisk.

Start eksempelvis med S&P 500, Oslo Børs eller et utvalg store aksjer. Implementer noen enkle strategier:

- Moving-average crossover
- RSI
- MACD
- Momentum
- Bollinger Bands
- Breakout-strategier

Sammenlign strategiene med en buy-and-hold-portefølje.

Det sentrale spørsmålet skal ikke bare være hvilken strategi som gir høyest avkastning. Gruppen bør undersøke risiko, drawdowns, volatilitet, Sharpe ratio og hvor ofte strategiene faktisk handler.

### Viktig faglig del

Prosjektet gir en svært god introduksjon til forskjellen mellom **in-sample** og **out-of-sample** analyse.

En strategi kan se fantastisk ut dersom parameterne er valgt etter at man har sett historiske data. Gruppen bør derfor dele datasettet i trenings- og testperioder og undersøke om strategiene fortsatt fungerer på data de ikke ble utviklet på.

Transaksjonskostnader kan også inkluderes, for å gjøre testen mer realistisk.

### Mulige avanserte utvidelser

Eldre studenter kan undersøke:

- statistisk signifikans av meravkastningen
- bootstrap av strategiresultater
- parameterstabilitet
- walk-forward testing
- multiple-testing-problemet
- hvordan resultatene varierer mellom bull- og bear-markeder

### Kobling til ITØK

Prosjektet kombinerer programmering, statistikk og økonomisk teori og er derfor spesielt godt egnet som et første prosjekt for en blandet gruppe.

**Sluttleveranse:** Et lite Python-bibliotek for backtesting og en rangering av hvilke tekniske strategier som faktisk overlever realistiske tester.

## 2. Momentum: finnes markedets mest kjente anomalie fortsatt?

**Passer for:** 2.–4. kull, men 1. kull kan bidra  
**Gruppestørrelse:** 3–5  
**Tema:** Faktorinvestering, porteføljer, statistikk

### Prosjektidé

Momentum innebærer grovt sett å kjøpe verdipapirer som nylig har gjort det bra og selge eller unngå dem som nylig har gjort det dårlig.

Gruppen skal undersøke om en enkel momentumstrategi fungerer i et valgt aksjemarked.

Et mulig oppsett er å rangere aksjer hver måned basert på avkastningen de siste 3, 6 eller 12 månedene. Deretter konstrueres en portefølje av de sterkeste aksjene.

Studentene kan sammenligne ulike valg:

- 3 mot 6 mot 12 måneders momentum
- månedlig og kvartalsvis eller oftere rebalansering
- topp 5, 10 eller 20 prosent av aksjene
- likevektet mot markedsverdivektet portefølje

### Analyse

Strategien sammenlignes med markedsindeksen ved hjelp av blant annet:

- annualisert avkastning
- volatilitet
- Sharpe ratio
- maksimal drawdown
- turnover

En viktig del av prosjektet er å undersøke **hvorfor** momentum eventuelt fungerer. Gruppen kan diskutere hypoteser som investoradferd, treg informasjonsbearbeiding og risiko.

### Avansert spor

3.–4. kull kan teste om momentumavkastningen kan forklares av kjente risikofaktorer, undersøke momentum-crashes eller estimere regresjonsmodeller.

Man kan også teste «cross-sectional momentum» mot «time-series momentum».

### Hvorfor dette passer godt

Prosjektet kan gjøres forholdsvis enkelt, men kan samtidig utvikles til et ganske seriøst empirisk finansprosjekt.

**Sluttleveranse:** En forskningsrapport med konklusjonen: «Ville en investor faktisk kunnet implementere denne strategien?»

## 3. Bygg deres egen portefølje

**Passer for:** 2.–4. kull  
**Gruppestørrelse:** 4–6  
**Tema:** Porteføljeteori, optimering, risikostyring

### Prosjektidé

Gruppen får i oppgave å etablere et hypotetisk fond.

Fondet skal investere i eksempelvis 20–50 aksjer, ETF-er eller andre likvide aktiva. Gruppen må selv bestemme investeringsunivers, strategi og regler. Kan være interessant å teste denne på porteføljen til Fintech Enigma.

Deretter skal de konstruere flere porteføljer:

- Likevektet portefølje
- Minimum-variance-portefølje
- Maximum Sharpe-portefølje
- Risk-parity-portefølje

Prosjektet gir en naturlig inngang til matematisk optimering.

### Problemstillinger

Hvor mye betyr egentlig porteføljeoptimeringen?

Er avanserte modeller bedre enn en enkel 1/N-portefølje?

Hvor stabile er porteføljevektene når forventet avkastning eller kovariansmatrisen endrer seg litt?

Dette er viktig fordi klassisk porteføljeteori kan produsere svært ekstreme porteføljer når parameterestimatene er usikre.

### Avanserte utvidelser

Gruppen kan implementere:

- short-sale constraints
- maksimumsvekt per aksje
- sektorbegrensninger
- transaksjonskostnader
- shrinkage av kovariansmatrisen
- Black–Litterman
- rolling optimization

**Sluttleveranse:** Et investeringsmandat, en implementert porteføljemodell og en presentasjon som om gruppen skulle pitche fondet til investorer.

## 4. Kan maskinlæring predikere morgendagens aksjeavkastning?

**Passer for:** 3.–4. kull  
**Gruppestørrelse:** 3–5  
**Tema:** Machine learning, prediksjon, finansielle tidsserier

### Prosjektidé

Dette er et klassisk problem hvor det er svært lett å lage en modell som ser imponerende ut, men mye vanskeligere å lage en modell som faktisk predikerer fremtidige markedsbevegelser.

Målet er å predikere enten:

- neste dags avkastning
- retningen på markedet
- neste ukes avkastning

Mulige features kan inkludere:

- historiske avkastninger
- volatilitet
- volum
- RSI/MACD
- glidende gjennomsnitt
- markedsavkastning
- renter eller andre makrovariabler

Start med enkle modeller som lineær/logistisk regresjon. Sammenlign deretter med eksempelvis random forest, gradient boosting eller nevrale nettverk.

### Hovedpoenget

Prosjektet skal ikke bli en konkurranse om høyest accuracy.

Gruppen må spørre:

Gir modellen økonomisk verdi?

En klassifikasjonsmodell med 52 % accuracy kan potensielt være interessant dersom feilene og gevinstene er asymmetriske.

Omvendt kan 60 % accuracy være verdiløst dersom modellen lider av look-ahead bias.

### Viktige konsepter

- train/test split for tidsserier
- overfitting
- data leakage
- feature engineering
- walk-forward validation
- benchmark-modeller

### Avansert spor

Undersøk feature importance, SHAP eller hvordan modellen oppfører seg i ulike markedsregimer.

**Sluttleveranse:** En «ML trading research pipeline» med tydelig dokumentasjon av hvilke modeller som faktisk fungerer out-of-sample.

## 5. Markedsregimer: kan en algoritme oppdage bull- og bear-markeder?

**Passer for:** 2.–4. kull  
**Gruppestørrelse:** 3–5  
**Tema:** Clustering, tidsserier, makrofinans

### Prosjektidé

Finansmarkedet oppfører seg ikke nødvendigvis likt hele tiden. Perioder med stabil vekst kan etterfølges av perioder med høy inflasjon, kriser eller kraftige børsfall.

Gruppen skal undersøke om slike **markedsregimer** kan identifiseres automatisk.

Variabler kan være:

- aksjeavkastning
- volatilitet
- renter
- kredittspreader
- inflasjon
- arbeidsledighet
- oljepris

En enkel versjon kan klassifisere perioder etter faste regler.

En mer avansert versjon kan bruke clustering, Gaussian Mixture Models eller Hidden Markov Models.

### Forskningsspørsmål

Finnes det tydelige statistiske markedsregimer?

Hvor lenge varer de?

Hvordan oppfører ulike aktivaklasser seg i hvert regime?

Kan man lage en portefølje som endrer eksponering når regimet endres?

### Eksempel

Gruppen kan oppdage et «risk-on»-regime med høy aksjeavkastning og lav volatilitet og et «stress»-regime med negativ aksjeavkastning og høy volatilitet.

Deretter undersøkes om strategisk allokering mellom aksjer, obligasjoner, gull og kontanter kan forbedres.

**Sluttleveranse:** En interaktiv tidslinje/dashboard over markedsregimer og en analyse av investeringsimplikasjonene.

## 6. Volatilitetsprognoser: hvor risikabel blir neste uke?

**Passer for:** 2.–4. kull  
**Gruppestørrelse:** 2–4  
**Tema:** Tidsserier, risiko, økonometri

### Prosjektidé

Volatilitet er en av de viktigste størrelsene innen finans. Den brukes blant annet i risikostyring, derivatprising og porteføljekonstruksjon.

Gruppen skal forsøke å predikere fremtidig volatilitet.

Start med svært enkle modeller:

- historisk standardavvik
- rolling volatility
- exponentially weighted volatility

Deretter kan mer avanserte grupper implementere ARCH/GARCH eller maskinlæringsmodeller.

### Spørsmål

Hvilken metode gir best prognose?

Fungerer modellen like godt i rolige markeder som under finansielle kriser?

Hvor raskt reagerer den når volatiliteten plutselig øker?

Gruppen kan teste modellen rundt perioder som finanskrisen, pandemien eller andre turbulente markedsperioder.

### Praktisk anvendelse

Lag deretter en strategi hvor porteføljens eksponering reduseres når forventet risiko øker.

Dette kan eksempelvis være en enkel volatility-targeting-strategi.

**Sluttleveranse:** En modell som daglig beregner forventet volatilitet samt et dashboard som viser risikonivået i markedet.

## 7. Event study: hvordan reagerer markedet på nyheter?

**Passer for:** 1.–4. kull  
**Gruppestørrelse:** 3–5  
**Tema:** Statistikk, økonometri, markedseffisiens

### Prosjektidé

Hvor raskt reagerer aksjemarkedet på ny informasjon?

Gruppen velger én type hendelse, for eksempel:

- kvartalsrapporter
- rentebeslutninger
- oppkjøpsannonseringer
- CEO-bytter
- utbytteendringer
- indeksinkludering
- aksjesplitt

Deretter gjennomføres en klassisk event study.

Gruppen estimerer forventet avkastning før hendelsen og beregner abnormal returns rundt eventdatoen.

### Eksempel

Hvis Norges Bank overrasker markedet med en renteendring, reagerer norske banker annerledes enn andre selskaper?

Eller:

Hva skjer med aksjekursen når et selskap rapporterer et resultat som er vesentlig bedre enn forventet?

### Faglig læring

Prosjektet gir en svært fin introduksjon til hypotesetesting og markedseffisiens.

Førsteklassinger kan samle data og visualisere kursutviklingen, mens eldre studenter kan implementere statistiske tester og regresjonsmodeller.

### Avansert spor

- cross-sectional regresjon
- forskjeller mellom sektorer
- heterogenitet etter størrelse
- bootstrap confidence intervals
- kontroll for markedsavkastning

**Sluttleveranse:** En forskningslignende analyse som kunne vært utgangspunkt for en bachelor- eller masteroppgave.

## 8. Sentimentanalyse: kan finansnyheter predikere markedet?

**Passer for:** 2.–4. kull  
**Gruppestørrelse:** 3–6  
**Tema:** NLP, machine learning, alternativ data

### Prosjektidé

Finansielle markeder påvirkes ikke bare av tall, men også av hvordan informasjon kommuniseres.

Gruppen skal bygge en modell som måler sentiment i finansielle tekster.

Mulige datakilder:

- finansnyheter
- selskapsmeldinger
- kvartalsrapporter
- Reddit
- analytikerkommentarer

Start med en enkel ordlistebasert metode hvor positive og negative finansord telles.

Deretter kan gruppen sammenligne dette med moderne NLP-modeller.

### Problemstilling

Er negativt sentiment etterfulgt av negativ avkastning?

Har sentiment større sammenheng med volatilitet enn med avkastning?

Kan sentiment rundt et enkelt selskap brukes til å predikere kursbevegelser?

### Viktige metodiske problemer

Prosjektet bør diskutere kausalitet.

En negativ nyhetsartikkel publiseres ofte fordi aksjekursen allerede har falt. Korrelasjon betyr derfor ikke nødvendigvis at nyheten forårsaket kursfallet.

### Avansert spor

Sammenlign generelle språkmodeller med modeller tilpasset finansspråk, eller bygg en enkel tradingstrategi basert på sentiment.

**Sluttleveranse:** En sentimentindeks og visualisering av hvordan den samvarierer med finansmarkedene.

## 9. Norske renter, kronekurs og Oslo Børs

**Passer for:** 1.–4. kull  
**Gruppestørrelse:** 3–5  
**Tema:** Makroøkonomi, økonometri, finans

### Prosjektidé

Dette prosjektet tar utgangspunkt i norsk økonomi.

Gruppen undersøker sammenhengene mellom:

- styringsrente
- NOK/EUR eller NOK/USD
- oljepris
- inflasjon
- Oslo Børs

Første del kan være rent deskriptiv: Hvordan har variablene utviklet seg, og hvilke perioder skiller seg ut?

Deretter kan gruppen teste sammenhenger statistisk.

Eksempel:

Hvordan påvirkes kronekursen når norske renter endres relativt til renter i euroområdet eller USA?

Eller:

Har oljeprisen fortsatt stor betydning for NOK?

### Metoder

Nybegynnere kan arbeide med korrelasjoner og visualisering.

Viderekomne kan bruke:

- multippel regresjon
- laggede variabler
- tidsseriemodeller
- event studies rundt rentemøter
- VAR-modeller

### Hvorfor prosjektet er godt

Prosjektet kobler ITØKs makroøkonomiske teori direkte mot programmering og empiriske data.

**Sluttleveranse:** En norsk «macro-finance monitor» som automatisk oppdaterer sentrale indikatorer.

## 10. Faktorinvestering: bygg en norsk multifaktormodell

**Passer for:** 3.–4. kull  
**Gruppestørrelse:** 3–5  
**Tema:** Asset pricing, økonometri, investering

### Prosjektidé

Gruppen undersøker om systematiske selskapskarakteristikker kan forklare forskjeller i aksjeavkastning.

Mulige faktorer:

- value
- momentum
- size
- quality
- low volatility

Studentene konstruerer porteføljer basert på én eller flere faktorer og undersøker historisk avkastning.

### Eksempel

Ranger norske aksjer etter P/B eller P/E og sammenlign billige og dyre selskaper.

Deretter kan samme prosedyre gjennomføres for momentum.

Til slutt konstrueres en multifaktorportefølje.

### Analyse

Interessante spørsmål er:

Er faktorene korrelerte?

Finnes meravkastningen fortsatt de siste årene?

Er resultatet robust mot transaksjonskostnader?

Hvor høy turnover krever strategien?

### Avansert spor

Eldre studenter kan implementere faktorregresjoner og undersøke alpha og factor exposures.

En ekstra interessant del er å sammenligne amerikanske og norske markeder.

**Sluttleveranse:** Et «Enigma Factor Index» med dokumenterte investeringsregler.

## 11. Pairs trading og statistisk arbitrasje

**Passer for:** 2.–4. kull  
**Gruppestørrelse:** 2–4  
**Tema:** Statistikk, tidsserier, trading

### Prosjektidé

Pairs trading bygger på ideen om å finne to verdipapirer som historisk beveger seg sammen.

Hvis prisene plutselig divergerer, kjøper strategien den relativt billige og selger den relativt dyre.

Gruppen kan begynne med å finne kandidatpar gjennom korrelasjon.

Eksempler kan være selskaper fra samme industri eller ETF-er med lignende eksponering.

### Enkel strategi

Beregn forholdet mellom prisene.

Beregn deretter rolling mean og standardavvik.

Når spreaden beveger seg mer enn eksempelvis to standardavvik fra normalen, åpnes en posisjon.

Når spreaden normaliseres, lukkes den.

### Det interessante problemet

Høy korrelasjon betyr ikke nødvendigvis at to prisserier har et stabilt langsiktig forhold.

Dette åpner for videre analyse av stationaritet og cointegration.

### Avansert spor

- Augmented Dickey-Fuller
- cointegration
- Kalman filter
- dynamisk hedge ratio
- porteføljer med flere enn to aktiva

Gruppen bør også undersøke om strategien forsvinner etter transaksjonskostnader.

**Sluttleveranse:** En «pair finder» som automatisk søker gjennom et investeringsunivers og identifiserer kandidater for statistisk arbitrasje.

## 12. Value at Risk: hvor galt kan det gå?

**Passer for:** 2.–4. kull  
**Gruppestørrelse:** 2–4  
**Tema:** Risiko, sannsynlighet, simulering

### Prosjektidé

Banker og investeringsfond må ha modeller for hvor mye penger de potensielt kan tape.

Gruppen bygger et risikosystem for en hypotetisk portefølje.

Start med Value at Risk (VaR).

Sammenlign minst tre metoder:

- parametrisk VaR
- historical simulation
- Monte Carlo simulation

### Eksempel

Systemet kan rapportere:

Med 99 % konfidens forventer modellen at porteføljen ikke taper mer enn X kroner neste handelsdag.

Deretter skal studentene undersøke hvor ofte denne påstanden faktisk brytes historisk.

### Kritisk analyse

Finanskriser viser hvorfor normale fordelingsantakelser ofte er problematiske.

Gruppen bør derfor undersøke:

- fat tails
- skewness
- korrelasjoner under kriser
- Expected Shortfall

### Avansert spor

Lag stress-scenarioer:

- aksjemarked −20 %
- olje −30 %
- NOK kraftig svekket
- renter +200 basispunkter

**Sluttleveranse:** Et mini-risikostyringssystem tilsvarende noe man kunne sett hos et fond eller i en bank.

## 13. Kryptomarkeder: effektive markeder eller et paradis for tradere?

**Passer for:** 1.–4. kull  
**Gruppestørrelse:** 3–5  
**Tema:** Fintech, krypto, statistikk, markedsstruktur

### Prosjektidé

Kryptomarkedet gir tilgang til store mengder høyfrekvente data og handles døgnet rundt.

Gruppen undersøker om kryptomarkedet viser sterkere mønstre enn tradisjonelle finansmarkeder.

Mulige hypoteser:

- Bitcoin har sterkere momentum enn aksjer.
- Volatiliteten varierer gjennom døgnet.
- Weekend-effekter eksisterer.
- Handelsvolum kan predikere volatilitet.
- Krypto reagerer annerledes på makroøkonomiske nyheter enn aksjer.

### Første del

Analyser Bitcoin og Ethereum og sammenlign:

- avkastningsfordeling
- volatilitet
- drawdowns
- autocorrelation
- handelsvolum

Sammenlign deretter med S&P 500.

### Avansert spor

Studenter med mer erfaring kan undersøke:

- cross-exchange prisforskjeller
- funding rates
- futures versus spot
- volatilitet
- market microstructure

Prosjektet kan kobles direkte til spørsmål om finansiell teknologi og hvordan desentraliserte markeder skiller seg fra tradisjonell finans.

**Sluttleveranse:** En empirisk analyse av hvor «effektivt» kryptomarkedet faktisk ser ut til å være.
