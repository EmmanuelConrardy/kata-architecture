# Kata Architecture OhMyFood!

```
How do we get great designers?
Great designers design, of course. 
  --Fred Brooks
```

Les kata d'architecture sont prévus pour un groupe de 3 à 5 personnes. L'animateur gère la time-box et facilite l'exercice. Un projet ou un exercice est asigné à chaque groupe.

Pour que l'exercice soit profitable il convient de respecter quelques règles:
Les règles sont consitutés au fur et à mesure des phases de l'exercice, cependant l'animateur pourra vous répondre pour tous les points qui ne sont pas couvert par les règles.

## Phase constitution des équipes - 10 mins

Veuillez essayer de ne pas vous mettre avec un connaissance ou quelqu'un avec qui vous avez l'habitude de travailler.
Vous n'aurez pas besoin d'ordinateur à ce moment, en revanche l'utilisation de bloc-note, tableaux ou autres moyens collabortif est fortement recommandés premier arrivé premier servie.
Une fois que votre équipe est constituée vous pouvez passer à la phase suivante.

## Phase de discussions et design - 2x30mins

C'est le moment de découvrir le domaine métier et les stratégies de l'entreprise.
vous pouvez poser toutes les questions à l'animateur il jouera le rôle du client, du CEO, de l'Ops, Tech lead,...
Toutes les technologie sont acceptées. Le client ne s'en préoccupe pas vraiment si vous pensez que c'est le bon choix allez y mais soyez prêt à le defendre.
Vous ne pouvez pas supposer que vous avez une équipe parfaite, veuillez supposer que l'équipe est au moins aussi talentueuse que les équipes avec lesquelles vous travaillez regulièrement.
Choississez une strategie et proposer une ou des architectures pour soutenir cette stratégie.

On attent une compréhension des préoccupations des parties prenantes, la présentation des attributs qui vont être selon vous necessaire. Une présentation de la version du système à atteindre et de la cible organisationelle.

## Phase de revue - 30 mins

C'est le moment où vous allez présenter votre architecture aux autres groupes. L'animateur peut prendre le rôle du client si c'est necessaire. Ceux qui assiste à la présentation devront poser des questions sur la compréhension du projets et les choix architecturaux.
Si il y a confusion ou désacord l'animateur se garde le droit de clarifier ou mettre fin au débat.
 
## La phase des votes - 5 mins

3 points : si vous pensez que l'équipe à reussi l'exercice, ils n'ont pas forcement encore répondu à toutes les attentes mais ils sont sur la bonne voie.
2 points : Il y a quelques oublies qui vous font pensez qu'il y a encore des efforts à faire afin d'avoir une bonne vision de ce que l'équipe souhaite réaliser.
1 point : Vous pensez que c'est irréalisable dù a de trop grande suppositions où que la proposition est une très mauvaise idée en tout cas pour vous, c'est non.

Le but est de s'entrainer à produire et transmettre un design et/ou architecture de la manière la plus clair possible.
Répondre à une liste de besoin fonctionnel et technique et de savoir argumenter nos choix.
Il faudra savoir doser nos ambition pour trouver le bon équilibre d'effort qui pourra être porté par l'équipe et
accorder les parties prenante sur une architecture qui soutiendra leurs projets.

## OhMyFood!

Specialiste de la livraison de plat à domicile depuis 2005. Hervé le gérant était traiteur quand il a lancé
OhMyFood! il a décidé de lancer une plateforme via un CMS qui permet à ses clients de commander directement chez des  restaurants partenaire.

Après quelques années et un chiffre d'affaire grandissant il decide d'embaucher une équipe à temps plein, l'entreprise propère et developpe un système un peu plus specialisé.
Mais l'ombre de très grand concurrent qui vont arriver d'ici un ou deux ans inquiète.
Ils vont devoir faire des choix difficiles pour sortir leur épingle du jeux.

Voici la liste principale des préoccupation des parties prenantes.

les client "Commandent" : 

Commander un plat en moins de 45 mins.
Payer d'une manière simple et securisé.
Pouvoir suivre sa commande et savoir quand elle va arriver.

les livreurs "livrent":

Etre prevenue 15 mins avant si il y a une commande à recupérer.
Avoir les informations précise de la livraison sur son téléphone.
Pouvoir appeler le client / le restaurnt / le support en cas de problème.

les restaurants "cuisinent" :

Pouvoir recuperer facilement la commande pour la transmettre en cuisine
Pouvoir mettre à jour la carte en fonction des menus et des stocks
Pouvoir contacter facilement un livreur si besoin.

La plateforme OhMyFood "Apporte des clients":

Traiter les commandes automatiquement avec le moins d'anomalies
Envoyer des emails et sms personalisées pour acquérir et fideliser le client
Récupérer les frais de gestion et commissions des restaurants.

- Contexte : équipe de 15 personnes
- UX/UI : Creation de maquette et des pages html/css
- Devs : Strategie de déploiment monolitique
- Commerce : S'occupe du parc de restaurants (contrat, suivie, mise en avant)
- Marketing : S'occupe des analytiques, Seo, de rapporter du traffic, d'envoyer des sms et emails specialisés.
- Comptabilité : S'occupe des factures des restaurants (frais, commission) et des remboursement des clients.
- RH : S'occupe de la gestion administrative des employés
- C-level : S'occupe de la stratégie de l'entreprise et de faire une veille sur le marché de la livraison de plat à domicile.
- Service client : utilisteur du backoffice il s'occupe de gérer les problème lors de la livraison.

## Applications OhMyFood!

- Repartie sur 3 serveurs en F5

- Une application mobile native IOS/Android faite par une agence. ~ une livraison mois

- Un site web, un CMS + des plugin specialisés ~ une livraison semaine
(Catalogue restaurant, tunnel d’achat, compte client)

- Un site web portail restaurant (réception de la commande, changement de carte, horaire) ~ une livraison mois

- Un backoffice (provisionning, gestion utilisateur,…) ~ une livraison an

- Un base de donnée pour la comptabilitée et un base de données pour le reste.

## Climat de l'entreprise et du marché: 

On parle d'un rachat de OhMyFood! par une entreprise qui souhaite diversifier ses offres.
Des acteurs majeures de la livraison devraient arriver d’ici un an ou deux sur le même segment.
Le secteurs subit de plus en plus de fraude à la carte bleue.

### Historique :

Il y a des pic de commandes (saint Valentin, foot, dimanche,…) et le site à du mal à tenir la charge.
Les restaurants réclament plusieurs changements sur le portail restaurant pour interagir plus facilement ou se brancher à leur logiciel de caisse
Les restaurants souhaitent améliorer leur visibilité « propre » sur le web.
Les clients souhaitent commander d'une manière plus fluide et payer facilement.

Pour rester compétitif divers stratégies sont envisagées : 

  Stratégie Focus restaurant (commerce) : Devenir l'acteur incontournable du logiciel de caisse spécialisé avec une gestion unique des flux de commandes en ligne / base client / gestion des promotions spécialisées / vente en ligne des plats qui vont être gâcher.

  Stratégie Focus client (marketing) : une expérience soignée multiplateforme / suivie de commande temps réel / paiements différés / garantie commande sans erreur

  Stratégie Saas (Devs) : Mise en place d'un abonnement, mini-site en marque blanche à la minute / inscription / gestion des restaurants par les restaurants avec des API / webhooks des evènements / internationalisation

## Chiffres

- Base ~ 2500 restaurants
- Client par mois ~ 30000 (pour un trafic unique de 300000) 
- CA : 2M
- Effort tech : 400000 €
- Effort marketing : 200000 €
- Effort commercial : 300000 €
- Autres : 150000€

## Votre mission

Proposer une architecture pour soutenir la ou les stratégies tech, marketing ou commerciales.
