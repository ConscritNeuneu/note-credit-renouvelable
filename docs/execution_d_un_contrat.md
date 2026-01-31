# Étude d'un contrat de crédit renouvelable

## Contexte

Nous souscrivons à un crédit renouvelable auprès d'un grand
établissement bancaire. Le compte a été utilisé avec quelques débits et
remboursements afin de comprendre la logique de calcul des intérêts.

## Éléments contractuels

## Utilisation

### Relevés

Les relevés de janvier et février permettent de bien appréhender la
mécanique du compte.

[À venir]

### Recalcul des intérêts.

[À venir]

### Analyse du fonctionnement

- Il s'agit vraisemblablement d'un compte double, un pour le capital emprunté
  et un pour les intérêts. L'absence de date sur la ligne intérêts indique
  vraisemblablement que la valeur n'est pas affectée au compte de capital.

- Néammoins pour les besoins d'affichage, à la fois le capital emprunté et
  les intérêts calculés sont rassemblés dans une seule valeur pour l'édition
  du relevé sous le terme « nouveau montant utilisé ».

- Les intérêts sont très vraisemblablement calculés une fois par période, au
  moment du relevé, par un moteur d'agios bancaire classique calculant une
  échelle d'intérêts selon la méthode hambourgeoise. La mention « Taux
  mensuel de la période » laisse penser que le moteur n'est capable
  d'appliquer qu'un seul taux journalier. Le moteur est chargé avec un relevé
  de transactions synthétique correspondant à la période selon la date de
  valeur de chaque opération. Le relevé synthétique démarre à l'ouverture
  comptable de la période et se termine à la date prévisible de la mensualité
  automatique.

- Le taux chargé dans le moteur d'agios est vraisemblablement
  t/12/nb_jours_mois, le taux de base étant très probablement celui
  correspondant au solde en fin de période.

- Les intérêts sont liquidés au moment de la mensualité, la banque s'y
  engageant au moment du relevé.

- Comme on observe un précompte d'intérêts entre la date du relevé et la
  date de la mensualité prévue, cela implique que pour la période suivante la
  date de valeur du transfert du solde est paramétrée au 3 du mois pour faire
  soudure entre les périodes. Les débits apparaîssant avant cette soudure sont
  comptabilisés normalement.

- La date de valeur des opérations carte est au moment de la date de
  transaction, non la date de comptabilisation.

- Étant donnés la séparation probable des comptes et la date de valeur de
  rollover de la dette fixée au 3 du mois, et malgré l'intégration apparente
  dès le relevé de compte des intérêts on peut écarter une suspicion
  d'anatocisme. Il serait appréciable que le relevé lève tout doute.

### Mécanisme des dates de valeur

[A venir]

## Discussion et synthèse

Points problématiques

- le contrat présente bien des effets de seuils au niveau des encours qui
  provoque des amortissements de fait usuraires (pour des encours partant au
  delà de 3k€). Une longue discussion ayant déjà été consacrée à ce point, il
  n'est pas utile de revenir dessus.
- fixation du taux débiteur journalier dépendant du mois, non explicité dans
  le contrat et produisant une charge de la dette non uniforme dans l'année
  (février est 10% plus cher que janvier).
- dates de valeur des débits non explicites pour les paiements carte, ce qui
  complique le recalcul des intérêts intercalaires pour le client. Du point
  de vue du client cette date de valeur peut se justifier car il a reçu un
  service en échange du paiement, mais du point de vue de la banque il
  s'agit d'une marge indue, les fonds n'ayant pas été décaissés avant la date
  comptable. Le système interbancaire assure ce crédit, déjà couvert par les
  frais carte bancaire supportés par le commerçant.
- précompte des intérêts sur une dizaine de jours entre l'édition du relevé
  (daté aux alentours du 25) et la mensualité le 3 du mois suivant. Ce délai
  n'est plus justifié dans l'environnement moderne SEPA (présentation au
  débit à D-1).
- En conséquence du précompte la date de valeur du rollover de la
  dette, fixée au 3 pour faire soudure avec le précompte des intérêts est non
  explicite et incompréhensible pour le client consommateur.
- En conséquence des deux points précédents, les remboursements anticipés
  entre le relevé et la mensualité sont bloqués artificiellement afin d'éviter
  d'accumuler des nombres négatifs en date de valeur (le solde synthétique en
  date de valeur démarre à zéro en début de période) et devoir potentiellement
  un remboursement d'intérêts indus. L'infraction n'est techniquement pas de
  l'usure, mais revient au même par le maintien artificiel d'une créance
  productive d'intérêts.
- séparation non explicite entre intérêts et capital emprunté dans les
  relevés « nouveau montant utilisé » ce qui laisse une suspicion
  d'anatocisme entre la date du relevé et la date de paiement des intérêts
  via la mensualité le 3.

## Refs légales

Dispositif non conforme au regard du code de la consommation.

[Article L312-34 du code de la consommation](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000032226120)

L'emprunteur peut toujours, à son initiative, rembourser par anticipation,
en partie ou en totalité, le crédit qui lui a été consenti. Dans ce cas, les
intérêts et frais afférents à la durée résiduelle du contrat de crédit ne
sont pas dus.


