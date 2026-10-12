---
title: "Teeterbrädans fysik"
subtitle: "Kontakt, rotation och arbete under ett belastat fall"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-12"
lang: sv
abstract: |
  Vi härleder mekanismen bakom del 1 av Mad Scientist 1, från ett illustrativt
  akrobathopp till den beräknade hävstången med två fallvikter. Oberoende
  integrationer ger mottagararbetet 6.994139 J och händelsens COP 1.188267.
  Kontakt, återstuds och förnyad kontakt förklarar överföringen. Vikternas
  fortsatta fall och slutliga energilager sluter arbetskontot. Figurer och
  tabeller knyter samman kraftlagar, rörelse och mätbara signaler.
keywords:
  - teeterbräda
  - ensidig kontakt
  - hävstångsdynamik
  - arbete och energi
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-teeterboard} (planerad; lokal utgåva)\par
\noindent Svensk utgåva av \href{../physics-teeterboard.pdf}{Physics of the teeterboard}.\par
\endgroup

# Från ett hopp till en fråga om arbete

Två personer landar på ena sidan av en teeterbräda och lyfter en tredje.
Stödet ändrar rörelsens riktning medan ben och bräda deformeras. Del 1 av
[Mad Scientist 1][companion] motiverar med denna bild en hävstång med fallvikter
[OP-CT-HW-01]. Akrobaternas hastigheter är illustrativa; den numeriska studien
gäller en separat mekanisk modell.

![Schematisk bild av det illustrativa hoppet. Inkommande och utgående rörelseenergi avser olika ändpunkter; kompression, tyngdkraft och eventuellt muskelarbete verkar däremellan.](figures/launch.pdf){#fig:launch width=98%}

Med tre lika massor $M=70\,\mathrm{kg}$, två inkommande hastigheter
$u=5\,\mathrm{m/s}$ nedåt och en utgående hastighet $w=8\,\mathrm{m/s}$ uppåt fås
\begin{equation}
K_{\rm in}=Mu^2=1750\,\mathrm J,\qquad
K_{\rm out}=\tfrac12Mw^2=2240\,\mathrm J,
\quad \frac{K_{\rm out}}{K_{\rm in}}=\frac{32}{25}.
\label{eq:launch}
\end{equation}
Skillnaden är $490$ J. Om de två massorna sjunker ytterligare $0.50$ m
frigörs $2Mg(0.50\,\mathrm m)=686.7$ J. Det visar tyngdkraftens möjliga
bidrag; den uppkastades höjning, kvarvarande rörelse, deformation, förluster
och aktivt arbete måste också ingå i ett fullständigt energikonto för hoppet.

\newpage

# Geometri och krafter i det beräknade förloppet

Beräkningen ersätter akrobaterna med två identiska, vertikalt styrda
fallvikter och en yttre viskös mottagare. Den stela brädan har en fast
vridpunkt, tröghetsmoment $I$, vridfjäder $K_\phi$ och lagerdämpning $c_b$.
Dess masscentrum ligger i vridpunkten. Kontaktkrafterna är vertikala och
ideala styrningar utför inget arbete. Brädböjning, en uppkastad akrobat och
aktiva benkrafter ingår inte i modellen.

![Modellen schematiskt under kontakt. Vikterna delar vänster hävarm men har var sin vertikal fjäder. Positiv rotation sänker denna arm och höjer mottagaren. Vridfjäder och lager verkar mot marken.](figures/model.pdf){#fig:model width=98%}

Vikternas höjder $y_i$ är positiva uppåt, och brädans vinkel är $\phi$.
En hävarm med tecken $a$ har höjden $a\sin\phi$; mottagarens förskjutning
är $s_R=a_R\sin\phi$. Geometrin ger kompression och mottagarhastighet:
\begin{equation}
\delta_i=[a\sin\phi-y_i]_+,\quad f_i=k\delta_i,\qquad
v_R=a_R\cos\phi\,\dot\phi,\quad F_R=bv_R.
\label{eq:contact}
\end{equation}
Här är $[x]_+=\max(x,0)$ och $F_R$ kraften som överförs till mottagaren.
Den motsatta kraften verkar på brädan. Varje vertikal kraft multiplicerad
med sin horisontella momentarm ger Newtons ekvationer:
\begin{equation}
\begin{split}
m\ddot y_i=-mg+f_i,\qquad i=1,2,\\
I\ddot\phi=-a\cos\phi(f_1+f_2)-K_\phi\phi-c_b\dot\phi
-b a_R^2\cos^2\phi\,\dot\phi.
\end{split}
\label{eq:newton}
\end{equation}

| Storhet | Värde | Storhet | Värde |
| :--- | ---: | :--- | ---: |
| Varje vikt $m$ | $1$ kg | Tröghetsmoment $I$ | $0.15$ kg m$^2$ |
| Vikternas arm $a$ | $-0.50$ m | Mottagararm $a_R$ | $0.80$ m |
| Kontaktstyvhet $k$ | $500$ N/m | Last $b$ | $32$ N s/m |
| Vridstyvhet $K_\phi$ | $50$ N m/rad | Dämpning $c_b$ | $0.10$ N m s/rad |
| Starthöjd $H$ | $0.30$ m | Tyngdacceleration $g$ | $9.81$ m/s$^2$ |

: Referensparametrar. Från början är $y_1=y_2=H$, $\phi=0$ och alla hastigheter noll. Händelsen slutar vid den fasta tiden $T=1.5$ s.

Fjädrarna trycker bara när de är komprimerade. Vid kontaktförlust är
$\delta_i=f_i=0$; lagen ger varken stötimpuls eller språngvis energiförlust.
Båda kontakterna är rent elastiska. Energi avges till mottagaren och som lagervärme.

\newpage

# Kontaktförloppet

Före första kontakten ligger brädan horisontellt och varje vikt faller fritt:
$y=H-gt^2/2$. Kontakten börjar vid $t_c=\sqrt{2H/g}=0.247310$ s,
med $\dot y(t_c)=-\sqrt{2gH}=-2.426108$ m/s. Symmetrin gör de två
kontakterna samtidiga. Krafterna bromsar vikterna och ger brädan ett positivt
vridmoment; höger arm lyfts mot mottagarens motstånd.

![Beräknat referensförlopp. Till vänster: vikternas, vänster brädkontakts och mottagarens höjder. Till höger: uppåtriktad kraft på varje vikt och kraft med tecken till mottagaren. Kontakten är öppen mellan de prickade linjerna.](figures/history.pdf){#fig:history width=98%}

\FloatBarrier

| Händelse | Tid (s) | Viktens $y$ (m) | Brädans $\phi$ (rad) |
| :--- | ---: | ---: | ---: |
| Första kontakt | 0.247310 | 0.000000 | 0.000000 |
| Vikten vänder första gången | 0.344255 | $-0.148164$ | 0.139293 |
| Brädan vänder första gången | 0.408321 | $-0.110027$ | 0.195639 |
| Kontakten öppnas | 0.427352 | $-0.095356$ | 0.191887 |
| Kontakten sluts igen | 0.526451 | $-0.074597$ | 0.149754 |
| Händelsens fastställda slut | 1.500000 | $-0.114406$ | 0.190618 |

: Numeriskt bestämda övergångar och den föreskrivna sluttiden. Vikterna och brädan byter riktning vid olika tidpunkter.

Vikterna når sitt lägsta läge medan brädan fortfarande roterar uppåt på
mottagarsidan. När fjädrarna avlastas lyfts vikterna. De lämnar brädan,
följer en kort kastbana och får kontakt igen. Mindre svängningar följer.
Den största kraften på varje vikt är $46.53$ N och den största kompressionen
$93.05$ mm; dessa värden är fjädermodellens förutsägelser.

Mottagarkraften byter tecken när mottagarhastigheten gör det, men effekten
är fortfarande $P_R=F_Rv_R=bv_R^2\geq0$. Även returrörelsen nedåt avger
alltså arbete. En enkelriktad mottagare eller fritt flygande akrobat kräver en annan lag.

Rörliga brädpunkter har $v_a=a\cos\phi\dot\phi$ och $|v_R/v_a|=a_R/|a|=1.6$. Här kan vikterna komprimera fjädrarna och lämna
kontakten, så deras hastighet skiljer sig från brädpunktens. Eftergivlighet
och tidsförlopp styr överföringen; enbart hävarmsförhållandet kan inte
förutsäga utgående rörelse eller arbete.

Ett stillastående idealt stöd ger impuls $J_O=\int F_O\,dt$ men inget arbete,
eftersom $P_O=F_Ov_O=0$. Akrobaternas vertikala rörelsemängd bevaras inte ensam.
Utgående hastighet avslöjar inte arbetets källa; kontaktförloppet visar
krafterna och förflyttningarna.

\newpage

# Arbetsbalansen härledd

Det mekaniska systemet omfattar vikter, bräda, kontaktfjädrar och vridfjäder,
med tyngdkraften representerad som lägesenergi. Mottagaren och lagervärmen
ligger utanför. Lägesenergins nollnivå är den ursprungliga horisontella brädan:
\begin{equation}
U=\tfrac12m\sum_i\dot y_i^2+\tfrac12I\dot\phi^2
+mg\sum_i y_i+\tfrac12K_\phi\phi^2+\tfrac12k\sum_i\delta_i^2.
\label{eq:store}
\end{equation}
Under kontakt gäller $\dot\delta_i=a\cos\phi\dot\phi-\dot y_i$.
Multiplicera \eqref{eq:newton} med respektive hastighet och derivera
\eqref{eq:store}: kontakt- och vridfjäderkrafternas effekter tar ut varandra
internt. Därmed fås
\begin{equation}
\dot U=-bv_R^2-c_b\dot\phi^2,\qquad
U(T)+W_R+Q_b=U(0),\quad
(W_R,Q_b)=\int_0^T(bv_R^2,c_b\dot\phi^2)\,dt.
\label{eq:work}
\end{equation}
Identiteten gäller även när kontakten öppnas och sluts, eftersom fjäderenergin
är noll vid noll kompression. Balansen följer av kraftlagarna.

![Beräknat ackumulerat mottagararbete och total mekanisk energi. Den senare omfattar lägesenergi med tecken. Summan av dessa två och lagervärmen förblir 5.886 J.](figures/energy.pdf){#fig:energy width=96%}

\FloatBarrier

| Energi eller arbete | Start (J) | Slut eller ackumulerat (J) |
| :--- | ---: | ---: |
| Lägesenergi | 5.886000 | $-2.244651$ |
| Rörelseenergi, båda vikterna och brädan | 0 | 0.000012 |
| Vridfjäder | 0 | 0.908383 |
| Båda kontaktfjädrarna | 0 | 0.193519 |
| Total mekanisk energi $U$ | 5.886000 | $-1.142737$ |
| Mottagararbete $W_R$; lagervärme $Q_b$ | 0; 0 | 6.994139; 0.034598 |

: Energilagren vid ändpunkterna beräknas direkt ur tillståndet; arbetet fås genom integration av effekten.

De ytterligare $2.244651$ J som frigörs under startplanet räcker till
$1.108139$ J utgående arbete utöver startreferensen, $1.101914$ J kvarvarande
rörelse- och fjäderenergi samt $0.034598$ J lagervärme. Mekanismens arbetskonto
sluter, med den negativa slutliga lägesenergin medräknad.

\newpage

# Vad kvoten och lasten ändrar

Ingen yttre aktuator driver denna händelse. Dess definierade nämnare för
startenergin är $D=2mgH=5.886$ J. Med exakt samma referens fås
\begin{equation}
C_{\rm event}=\frac{W_R}{D}=1.188267,\qquad
\eta_g=\frac{W_R}{mg\sum_i[y_i(0)-y_i(T)]}=0.860219.
\label{eq:ratios}
\end{equation}
Kvoterna besvarar olika frågor: utgående arbete relativt startplanets
energireferens, respektive den andel av den faktiska minskningen i lägesenergi,
$8.130651$ J, som når mottagaren. En flyttad nollnivå $y'=y-h$ ändrar $D$
till $D'=D-2mgh$ och $U(T)$ med samma konstant. Arbetet och $\eta_g$
ändras inte; $W_R/D'$ beror på referensen och kräver $D'>0$.

| $k$ (N/m) | $b$ (N s/m) | Mottagararbete (J) | Händelsens COP |
| ---: | ---: | ---: | ---: |
| 500 | 32 | 6.994139 | 1.188267 |
| 450 | 30 | 7.013120 | 1.191492 |
| 450 | 34 | 7.017282 | 1.192199 |
| 550 | 30 | 6.974505 | 1.184931 |
| 550 | 34 | 6.978687 | 1.185642 |

: Återberäkning av referensfallet och samtliga fyra bekräftelsefall i följeartikeln; händelsen och höjdreferensen hålls fasta.

![Beräknade lastjämförelser vid $k=500$ N/m. Högre motstånd ändrar kraftpulsen och fördröjer arbetsöverföringen; större kraft behöver inte ge mer arbete fram till 1.5 s.](figures/load.pdf){#fig:load width=98%}

\FloatBarrier

Vid $b=16,32,64$ N s/m blir arbetet $6.959211$, $6.994139$ respektive
$6.977427$ J. Vid $b=0$ är mottagararbetet noll och betydande rörelse återstår.
I belastad statisk jämvikt ger $f_i=mg$ att
$K_\phi\phi_*=-2amg\cos\phi_*$ och $y_*=a\sin\phi_*-mg/k$.
Referensvärdena är $\phi_*=0.192573$ rad och $y_*=-0.115313$ m,
nära men skilda från tillståndet vid den ändliga sluttiden.

Vi integrerade de symmetriska Newton-ekvationerna oberoende med två numeriska
metoder och förfinade tidssteg: 21 körningar för alla åtta konfigurationer.
Största spridningen i mottagararbete var $2.66\times10^{-7}$ J; största
energibalansrest var $3.22\times10^{-7}$ J. Oberoende effektkvadratur avvek
som mest $1.05\times10^{-11}$ J. Detta uppskattar numerisk känslighet, men
ger inga felgränser för en fysisk kontaktlag.

\newpage

# Mätningar och nästa händelse

En synkroniserad lastcell och lägesgivare ger mottagararbetet med tecken,
$W_R=\int F_R\,ds_R$, inklusive returrörelsen. Vikternas höjder och brädans
vinkel skiljer tyngdkraftens bidrag från kompression och kvarvarande rörelse;
enbart sluthastigheten räcker inte.

| Signal eller villkor | Referensförutsägelse eller antaget krav |
| :--- | :--- |
| Största mottagarkraft och hastighet | $52.40$ N; $1.637$ m/s |
| Mottagarens lägesintervall; total väg | $0$--$0.1555$ m; $0.2460$ m |
| Kontakt och händelsetider | Kontaktförlust $0.427$--$0.526$ s; slut $1.5$ s |
| Föreslagen registrering | $200$ Hz respons; $2$ kHz sampling; tidsskevhet $\leq0.1$ ms |
| Antagna samtidiga energifelgränser | $B_{\rm in}=0.02943$ J; $B_{\rm out}=0.06608$ J |

: Förutsagda signalnivåer och följeartikelns föreslagna instrumentbudget. Gränserna kräver kalibrering; de är inte mätresultat härifrån.

Budgeten omfattar startmassa och starthöjd, kraft- och lägesskalor,
nollpunktsfel, sampling, tidsfel, bandbredd, instrumentbelastning och
händelsegränser. Med dessa samtidiga gränser ligger referensresultatet över 1.15:
\begin{equation}
\frac{W_R-B_{\rm out}}{D+B_{\rm in}}=1.17118>1.15,
\qquad W_R-1.15D=0.225239\,\mathrm J.
\label{eq:measurement}
\end{equation}
Vikternas sluthöjd är lika avgörande att mäta: det förutsagda medelvärdet
ligger $0.114406$ m under startplanet. Där syns energin som utelämnas om
starthöjdens referens förväxlas med hela fallet.

## Förberedelse och återställning

Vid $T$ lutar brädan och kontakterna är komprimerade. En ny identisk
frigöring kräver återställning. Följeartikelns separat föreskrivna beräkning
av förberedelse och återställning ger kontot nedan.

| Intervall | Tillfört bruttoarbete (J) | Mottagararbete (J) |
| :--- | ---: | ---: |
| Förberedelse till angivet starttillstånd | 5.886000 | 0 |
| Händelsen på 1.5 s | 0 | 6.994139 |
| Föreskriven återställning | 2.210180 | 1.062185 |
| Hela förloppet | 8.096180 | 8.056324 |

: Bevarad beräkning av hela förloppet i följeartikeln. Total lagervärme är 0.039844 J och återfört aktuatorarbete 0.000012 J; start- och slutenergi är noll.

Kvoten för hela förloppet är $8.056324/8.096180=0.995077$: återställningen
tillför både ingående och utgående arbete, med andra ändpunktstillstånd än
i \eqref{eq:ratios}. Akrobathopp omfattar även benaktivering, brädböjning och
upphopp. I modellen styr kontaktelasticiteten överföringens timing, hävstången
ändrar riktningen och mottagaren tar arbete ur ett fall under startreferensen.

# Referens {-}

1. Hob Nilre och Bo C. Herlin (2026), *[Mad Scientist 1][companion]*,
   del 1, ”The falling-weight lever”, samt dess gemensamma simuleringskonto.

[companion]: https://github.com/hobnilre/physics-mad-scientist-1
