# Étude de l'exécution d'un contrat de crédit renouvelable

Points problématiques

- effets de seuils au niveau des encours qui provoque des amortissements
  de fait usuraires (pour des encours partant au delà de 6k€).
- fixation du taux débiteur journalier dépendant du mois, non explicité dans
  le contrat et produisant une charge de la dette non uniforme dans l'année
  (février est 10% plus cher que janvier).
- dates de valeur des débits non explicites pour les paiements carte, ce qui
  complique le recalcul des intérêts intercalaires pour le client.
- précompte des intérêts sur une dizaine de jours entre l'édition du relevé
  (daté aux alentours du 25) et la mensualité le 3 du mois suivant. Ce délai
  n'est plus justifié dans l'environnement moderne SEPA (présentation au
  débit à D-1).
- (en csq) la date de valeur du rollover de la dette (fixée au 3 pour faire
  soudure avec le précompte des intérêts) est non explicite et
  incompréhensible pour le client consommateur.
- (en csq) bloquage des remboursements anticipés entre le relevé et la
  mensualité pour éviter d'accumuler des nombres négatifs en date de valeur
  et devoir potentiellement un remboursement d'intérêts indus. L'infraction
  n'est techniquement pas de l'usure, mais revient au même par le maintien
  artificiel d'une créance productive d'intérêts.
- séparation non explicite entre intérêts et capital emprunté dans les
  relevés « nouveau montant utilisé » ce qui laisse une suspicion
  d'anatocisme entre la date du relevé et la date de paiement des intérêts
  via la mensualité le 3.

# Refs légales

Dispositif non conforme au regard du code de la consommation.

https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000032226120
[Article L312-34 du code de la consommation](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000032226120)

L'emprunteur peut toujours, à son initiative, rembourser par anticipation,
en partie ou en totalité, le crédit qui lui a été consenti. Dans ce cas, les
intérêts et frais afférents à la durée résiduelle du contrat de crédit ne
sont pas dus.


