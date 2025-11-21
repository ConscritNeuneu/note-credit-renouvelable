# Mise en pratique

## Introduction

Afin de rendre compréhensible le mécanisme qui conduit à des offres
usuraires, nous proposons de construire et comparer deux formules courantes:
le crédit amortissable et le crédit renouvelable « à paliers » tels qu'un
consommateur peut les trouver sur le marché français du crédit à la
consommation.

Les taux débiteurs seront communs aux deux offres et sont fixés au regard des
seuils d'usure du 4è trimestre 2025.

Le montant emprunté est choisi selon un scenario réaliste et de manière à
balayer l'ensemble du spectre des taux d'usure.

Nous étudierons trois scénarios d'utilisation:

- crédit amortissable de 6 500€ à taux fixe remboursable sur trois ans à
  mensualités fixes
- crédit in fine de 6 500€ à taux fixe sur trois ans
- crédit renouvelable « à paliers » de 6 500€ remboursé sur trois ans à
  mensualités fixes

Nous discuterons pour chaque scénario du prix total pour le consommateur ainsi
que le TAEG obtenu. Un tableau récapitulatif sera fourni en fin de document.

Nous montrerons enfin comment un prêteur peut, en adaptant une offre à paliers,
respecter l'esprit des réglementations sur l'usure.

## Construction des offres

### Seuils d'usure

Contrairement aux crédits immobiliers, les seuls d'usure pour les crédits à
la consommation—appelés« crédits de trésorerie » sont déterminés en fonction
du montant du crédit.

Ils sont publiés par la banque de France. Pour le 4è trimestre 2025 ils sont
disponibles sur la page
[Taux d'usure — 2025-Q4](https://www.banque-france.fr/fr/statistiques/taux-et-cours/taux-dusure-2025-q4)
et sont rappelés dans le tableau suivant:

| Catégorie | Taux moyen constaté au T3-2025 | Taux d'usure pour T4-2025 |
| --------- | ---------- | ------------ |
| Prêts d'un montant inférieur ou égal à 3 000 euros  | 17,62% | 23,49% |
| Prêts d'un montant supérieur à 3 000 euros et inférieur ou égal à 6 000 euros | 11,78% | 15,71% |
| Prêts d'un montant supérieur à 6 000 euros  | 6,55% | 8,73% |

Ces taux sont à comparer au TAEG (Taux Annualisé Effectif Global) du prêt
considéré.

### Taux débiteurs

#### Rappel sur le taux débiteur et le taux annualisé

Les crédits sont paramétrés en fonction du taux débiteur. Pour obtenir le
taux de période, qui est le coefficient multiplicateur appliqué au capital
après chaque période il est d'usage de diviser le taux par le nombre de
périodes dans une année.

Ex. un taux débiteur de 7,5% avec une périodicité de un mois aura un
coefficient multiplicateur de période de 1 + 7,5/1200 = 1,00625 soit un taux
de période de 6,25‰ (pour-mille).

Contrairement à un taux débiteur un taux annualisé tient compte des intérêts
composés sur un an, et donc la relation entre un taux débiteur et le taux
annualisé s'obtient par la formule suivante: (1 + t / p)^p - 1, t étant le
taux et p étant le nombre de périodes dans l'année. Ce taux annualisé
correspond à l'augmentation du montant emprunté dans le cas où le client ne
rembourserait rien pendant un an, laissant les intérêts capitaliser.

Sur l'exemple du prêt à 7,5% avec une période de un mois, le taux annualisé
sort à (1 + 7,5 / 1200)^12 - 1 = 7,76%.

Dans le cas des crédits de durée relativement faible cette différence n'est
pas significative pour comparer les coûts d'un crédit. C'est le cas des
crédits à la consommation.

Le point le plus important à retenir est que ce taux annualisé n'est pas
forcément égal au TAEG qui considère l'ensemble de la vie du crédit et en
incluant les frais prévisibles, il faut voir le TAEG comme le taux moyen sur
toute la vie du prêt.

#### Taux débiteurs appliqués

Pour fixer les idées nous proposons de construire l'exemple avec les taux
débiteurs suivants, qui sont choisis pour être environ 10% en dessous du
seuil d'usure :

| Montant emprunté   | Taux débiteur | Taux annualisé |
| ------------------ | ------------- | -------------- |
| m ≤ 3000€          | 19,33%        | 21,14%         |
| 3000€ < m ≤ 6000€  | 13,30%        | 14,14%         |
| 6000€ < m          | 7,59%         | 7,86%          |

## Scénarios d'usage

Le montant emprunté est de 6500€ et la durée de vie du prêt est de trois
ans, soit trente-six mois.

Rappel qu'un crédit fonctionne de la manière suivante. À la fin de chaque période
le capital est:

1. augmenté des intérêts
2. diminué du remboursement

Le paiement de la cotisation d'assurance est en sus.

Quand le remboursement est inférieur aux intérêts, l'amortissement est dit
négatif et le capital emprunté s'accroit; quand il est égal l'amortissement
est nul; et finalement quand il est supérieur l'amortissement est positif.

En cas d'événement intervenant en cours de période, des intérêts
dits « intercalaires » sont facturés. Pour simplifier nous n'allons pas
considérer cet événement, cela ne change les coûts que à la marge.

### Crédit amortissable à mensualités constantes

C'est la forme la plus courante du prêt, même si ce n'est pas la plus
simple à comprendre. Comme la mensualité est constante, au début cette
mensualité rembourse beaucoup d'intérêts—pusique le capital sur lesquels ils
s'appliquent est important—et moins de capital—pusique que la mensualité est
amputée des intérêts. À la fin les intérêts sont moindres puisque que le
capital restant est faible et donc la mensualité rembourse plus de capital.

Pour se faire une idée approximative du coût d'un prêt de ce type, on peut
considérer en première approximation que le capital « en moyenne » sur la durée du
prêt va être d'environ la moitié du capital emprunté, et que les intérêts
vont s'appliquer sur cette moitié de capital pour toute la durée du prêt.

La mensualité est calculable exactement, et fait intervenir la
[somme d'une série géométrique](https://fr.wikipedia.org/wiki/Mensualit%C3%A9).
Voir aussi cette page liée:
[Emprunts : mensualités, intérêt, taux, TEG, risque de taux](https://images-archive.math.cnrs.fr/Emprunts-mensualites-interet-taux-TEG-risque-de-taux.html?lang=fr)

Le capital emprunté K est de 6500€. Le taux de période est donc 7,59%/12 = 6,325‰

Ce capital se rembourse en 35 mensualités de 202,46€, et une dernière
mensualité de 202.41€. Le coût total du crédit est de 7288,51€. Le TAEG est
égal au taux débiteur annualisé, ici 7,86%.

### Crédit in fine

Le crédit in fine consiste à rembourser tout le capital en une fois à la fin
et ne payer que les intérêts à chaque fin de période.

Tel quel ce scénario est assez rare dans le cadre du crédit à la
consommation mais il est inclus ici car il maximise le coût d'un prêt pour
un certain taux. Pour les crédits auto il est courant de pratiquer un crédit
intermédiaire où une partie du capital est remboursé chaque mois et le
ballon correspondant à la valeur résiduelle du véhicule est soldé à la fin,
soit en rendant le véhicule, soit en payant le ballon: c'est la formule de
Location avec Option d'Achat.

Le coût total est typiquement le double du coût d'un crédit amortissable car
les intérêts s'appliquent sur la totalité du capital pendant toute la durée
du prêt, contrairement au crédit amortissable sur lesquels les intérêts
s'appliquent sur une portion qui diminue au fil du temps.

Ce cas est très facile à calculer car la mensualité est égale aux intérêts.

Le capital emprunté K est de 6500€. Le taux de période est donc 7,59%/12 = 6,325‰

Dans notre cas les intérêts reviennent à 6500 x 6,325‰ = 41,11€ ce qui
donne la mensualité.

Ce capital se rembourse en 35 mensualités de 41,11€, et une dernière de
6541,11€. Le coût total du crédit est de 7979,96€. Le TAEG est égal au
taux débiteur annualisé, ici 7,86%.

### Crédit renouvelable à paliers

Comme discuté dans la note principale, le prêteurs font varier le taux
débiteur selon l'encours sous le prétexte que le crédit est renouvelable.
Cela va conduire mécaniquement à un coût plus élevé des intérêts en fin de
prêt, quand le solde passe en dessous des seuils qui conduisent à des taux
élevés.

Trouver la mensualité constante n'est pas évident, il n'y a pas de relation
mathématique qui conduit au montant. Il faut procéder par approximation
successives.

Le capital emprunté est de 6500€

On trouve la mensualité constante 220,06€ par la méthode de la sécante.

Ce capital se rembourse en 35 mensualités de 220,06€ et une dernière de 218,43€.
Le coût total du crédit est de 7920,53€. Le TAEG pour cette opération est
calculé à 14.17%.

Le TAEG conventionnel est obtenu en remboursant sur 12 mois l'entièreté de
la ligne de crédit. Dans ce cas le capital est remboursé avec 11 mensualités
de 582,16€ et une dernière de 582,07€. Le coût total du crédit est de
6985,83€. Le TAEG pour cette opération est calculé à 14,39%. Comme on peut
le constater la différence de TAEG n'est pas significative.

Afin que le lecteur se rende bien compte du fonctionnement du prêt, le
tableau d'amortissement complet est reproduit [en annexe](#tableau-damortissement).
Il convient de prêter attention aux intérêts facturés à partir des échéances
n°4 et n°22: juste après l'échéance n°3, le capital emprunté passe en
dessous de 6500€, et de la même façon juste après l'échéance n°21 le capital
emprunté passe en dessous de 3000€.  Dans les deux cas les intérêts facturés
subissent un saut et l'amortissement diminue d'autant car le taux débiteur
est fonction de l'encours. La mensualité constante « cache » ce
fonctionnement.

Dans un crédit classique, on s'attend à ce que la proportion des intérêts
payés par la mensualité diminue avec le temps—on parle de comportement
monotone. Ce n'est absolument pas le cas ici.

## Tableau comparatif

| Scenario | Mensualités | Coût total du prêt | Intérêts | TAEG final | Note |
| -------- | ----------- | ------------------ | -------- | ---------- | ---- |
| Crédit amortissable | 202,46€ x 36 | 7288,51€ | 788,51€ | 7,86% | Crédit le moins cher |
| Crédit in fine | 41,11€ x 35 + 6541,11€ | 7979,96€ | 1479,96€ | 7,86% | Crédit le plus cher |
| Crédit renouvelable à paliers | 220,06€ x 36 | 7920,53€ | 1420,53€ | 14.17% | Offre usuraire |

On notera que l'amortissement du crédit renouvelable coûte quasiment aussi
cher qu'un crédit in fine, et de fait rien n'interdit à l'emprunteur de s'en
servir de cette façon en réutilisant le crédit de manière à rester dans la
tranche à taux la plus faible. Du point de vue du prêteur ce comportement
est à risque et devrait être pénalisé par une charge de la dette plus
élevée. Un client qui éteint sa dette au fur et à mesure diminue le risque
de défaut. Il est anormal d'obtenir un coût quasi identique en faisant
fonctionner le prêt dans cette configuration.

On notera enfin qu'un même TAEG peut cacher des disparités importantes de
charge de la dette selon la formule d'amortissement choisie, même pour une
durée égale.

## Conclusion

Appliquer un taux débiteur selon l'encours conduit à des offres
*grossièrement* usuraires. Ce type d'offre est selon nous insincère, induit
le consommateur en erreur sur les coûts réels et ne respecte pas ni l'esprit
ni la lettre de la réglementation sur l'usure.

Une manière simple pour un prêteur de construire une offre conforme à
l'usure, selon le TAEG conventionnel et selon les usages raisonnables,
consiste à geler le taux débiteur au moment de la dernière utilisation. La
phase d'amortissement qui suit devient alors celle d'un crédit à taux fixe
et mensualités constantes.

Cette manière de procéder est cohérente vis-à-vis du risque, car un crédit
en fin d'amortissement est moins risqué qu'un crédit en usage actif. De même
si vers la fin de l'amortissement le client réutilise sa ligne de crédit, il
est alors légitime qu'une nouvelle phase d'amortissement s'ouvre avec un
taux plus élevé car cette situation constitue une nouvelle prise de risque
pour le prêteur.

Bien sûr cette approche n'interdit pas au prêteur de réviser son abaque de taux,
conformément à l'article
[L.312-72 du code de la consommation](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000035731391).
Il convient évidemment dans cette hypothèse de vérifier que cela ne provoque
pas un comportement usuraire. Un amortissement démarré dans une des tranches
des tableaux d'usure doit y rester, tant que le client ne réutilise pas sa
facilité de crédit.

## Annexe

### Tableau d'amortissement

Tableau d'amortissement du crédit renouvelable sur 36 mois pour 6500€
empruntés et avec mensualité constante

| mois | décaissement | mensualité | intérêts | amortissement | capital restant | note |
| ---- | ------------ | ---------- | -------- | ------------- | --------------- | ---- |
|0|6500,00|0,00|0,00|0,00|6500,00||
|1|0,00|220,06|41,11|178,95|6321,05||
|2|0,00|220,06|39,98|180,08|6140,97||
|3|0,00|220,06|38,84|181,22|5959,75||
|4|0,00|220,06|66,05|154,01|5805,74|le taux passe de 7,59% à 13,30%|
|5|0,00|220,06|64,35|155,71|5650,03||
|6|0,00|220,06|62,62|157,44|5492,59||
|7|0,00|220,06|60,88|159,18|5333,41||
|8|0,00|220,06|59,11|160,95|5172,46||
|9|0,00|220,06|57,33|162,73|5009,73||
|10|0,00|220,06|55,52|164,54|4845,19||
|11|0,00|220,06|53,70|166,36|4678,83||
|12|0,00|220,06|51,86|168,20|4510,63||
|13|0,00|220,06|49,99|170,07|4340,56||
|14|0,00|220,06|48,11|171,95|4168,61||
|15|0,00|220,06|46,20|173,86|3994,75||
|16|0,00|220,06|44,28|175,78|3818,97||
|17|0,00|220,06|42,33|177,73|3641,24||
|18|0,00|220,06|40,36|179,70|3461,54||
|19|0,00|220,06|38,37|181,69|3279,85||
|20|0,00|220,06|36,35|183,71|3096,14||
|21|0,00|220,06|34,32|185,74|2910,40||
|22|0,00|220,06|46,88|173,18|2737,22|le taux passe de 13,30% à 19,33%|
|23|0,00|220,06|44,09|175,97|2561,25||
|24|0,00|220,06|41,26|178,80|2382,45||
|25|0,00|220,06|38,38|181,68|2200,77||
|26|0,00|220,06|35,45|184,61|2016,16||
|27|0,00|220,06|32,48|187,58|1828,58||
|28|0,00|220,06|29,46|190,60|1637,98||
|29|0,00|220,06|26,39|193,67|1444,31||
|30|0,00|220,06|23,27|196,79|1247,52||
|31|0,00|220,06|20,10|199,96|1047,56||
|32|0,00|220,06|16,87|203,19|844,37||
|33|0,00|220,06|13,60|206,46|637,91||
|34|0,00|220,06|10,28|209,78|428,13||
|35|0,00|220,06|6,90|213,16|214,97||
|36|0,00|218,43|3,46|214,97|0,00||

Ce tableau illustre que le coût du crédit ne suit pas une trajectoire
régulière : la proportion d'intérêts dans la mensualité peut augmenter en
cours de remboursement, phénomène incompatible avec la logique d'un
amortissement classique.
