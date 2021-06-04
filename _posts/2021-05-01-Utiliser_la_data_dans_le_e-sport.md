---
title: Usage de la data dans le Esport
description: 'Analyse de données du tournoi esport PUBG Global Invitational PGI.S'
lang: fr
image: /files/img/teamInCircle_FR.png
excerpt_separator: <!--more-->
---

Du 5 février au 28 mars 2021 s'est tenu en Corée du Sud le tournoi PGI.S qui a vu s'affronter 32 des meilleures équipes mondiales sur le jeu PlayerUnknown's Battlegrounds (PUBG).

<!--more-->

## A propos de PUBG

PUBG est un jeu de type *battle royale*. En esport, 16 équipes de 4 joueurs sont parachutées sur un terrain (*une map*). A intervalles réguliers, un cercle (*une zone*) apparaît qui rétrécit de plus en plus, qu'il faut rejoindre sous peine de voir la santé de son avatar décliner. Les joueurs peuvent être incapacités (*knocked*) mais réanimés (*revived*, ou encore *res* pour resurrected) par leurs coéquipiers si ceux-cis interviennent suffisamment rapidement. S'ils n'ont pas pu être réanimés, leur partie est terminée.  

L'équipe qui gagne le match est celle dont au moins un des membres est le dernier joueur en vie (*Top 1*), ayant survécu aux attaques des équipes concurrentes et aux dégâts subis en étant hors zone (*dans le bleu*).   

**Les différentes phases du jeu :**

- phase 0.1 = début du jeu, les joueurs sautent de l'avion et rejoignent la map
- phases entières (1, 2, 3...) = apparition du cercle
- phases se terminant par .5 (1.5, 2.5, 3.5...) = la zone de jeu se referme progressivement sur le cercle  

**Durée des phases et cercles consécutifs**

![](/files/img/phasesDurations_FR.png)



![](/files/img/consecutiveZones_FR.png)



## Les PGI.S et la "polémique WWCD"

Les PGI.S ont innové en créant des tournois hebdomadaires qui ont vu alterner des méthodes différentes pour en déterminer le vainqueur.

Depuis plusieurs années les principaux tournois utilisent les règles du jeu dites SUPER (pour *Standard and Universal PUBG Esports Ruleset*), qui entre autres précisent un système de points qui récompense le classement final à chaque match ainsi que le nombre d'adversaire éliminés (*kills*) au cours du match. Sans entrer dans le détail, une équipe qui finit un match en 3ème position en ayant réalisé 10 kills se voit attribuer le même nombre de points qu'une équipe ayant terminé en 1ère position avec 5 kills.

Dans le dispositif mis en place au cours des PGI.S, des tournois hebdomadaires *weekly survival* ont adopté un système récompensant exclusivement les équipes terminant en 1ère position (*WWCD* pour "Winner Winner Chicken Dinner", le texte que le vainqueur voit s'afficher sur son écran lorsqu'il gagne un match).

Pour les équipes, cela change la manière dont ils vont approcher les matchs.

La structure PUBG Esports annoncé début avril 2021 que le prochain tournoi PCS4 (*PUBG Continental Series 4*) suivrait le format WWCD, récompensant le nombre de Top 1 obtenus par chaque équipe, et ne comptabilisant les kills que pour départager les équipes ex-aequo. 

De façon assez véhémente, un certain nombre de joueurs professionnels ainsi que de fans exprime un fort rejet de ce format. Il lui est notamment reproché de ne pas récompenser la constance d'équipes qui régulièrement finissent parmi les mieux placées et font preuve de compétence dans leur capacité à éliminer leurs adversaires sans pour autant gagner les matchs, ainsi que de favoriser le hasard et la chance, arguant qu'une équipe parachutée à proximité de l'endroit où apparaîtra la dernière zone peut finir Top 1 sans avoir eu rien à faire pendant la quasi-totalité du match.

L'analyse des données des matchs de la PGI.S qui a vu co-exister les 2 types de fonctionnements doit permettre de tirer quelques enseignements à ce sujet.  

> Des limites possibles sont à considérer quant aux résultats de cette analyse :
>
> - Le format WWCD est tout neuf, inhabituel pour les équipes qui n'ont pas encore eu le temps d'y adapter leur style de jeu. De nouvelles metas apparaitront certainement à mesure que les pros vont s'y habituer et identifier de nouvelles façons de jouer plus à même de les faire gagner.
> - Lors de la PGI.S, le format WWCD permettait à des équipes de se qualifier pour la finale. Un seul Top 1 les qualifiait et ils n'avaient plus de match à jouer, ce qui est différent d'un tournoi où le classement final est déterminé en WWCD. Au-delà de nouvelles stratégies à l'échelle d'un match, ce sont également de nouvelles stratégies à l'échelle d'un tournoi qui vont se mettre en place.



## Etude des matchs de la PGI.S

### Nombre de matches

Un total de 220 matches de la PGI.S ont été analysés :
- 124 matches au format SUPER
- 96 matches au format WWCD



### Durée des matches

La durée moyenne des matches joués en format WWCD est légèrement plus élevée que celle des matches joués en format SUPER : 1870 secondes vs 1820 secondes

![](/files/img/matchDuration_FR.png)

En entrant un peu plus dans le détail, on observe qu'en effet 80% des matchs joués au format WWCD se terminent dans la dernière phase possible, là où ça n'est le cas que pour un peu plus de 60% des matchs joués au format SUPER.  

Dans tous les cas, la majorité des matchs se terminent dans cette phase 9.5.

![](/files/img/endPhases_FR.png)

*NB : la phase 9 ne dure que 10 secondes, ce qui explique les faibles pourcentages enregistrés*



### Nombre d'équipes  et de joueurs en vie par phase

Au format WWCD, en moyenne le nombre d'équipes en vie au début de chaque phase est plus important qu'avec le format SUPER, surtout en milieu de game entre les phases 4 et 8. Cette supériorité se tasse dans les phases finales.

![](/files/img/phaseTeamsAlive_FR.png)





### Nombre de kills par phase

Le nombre de kills par phase permet d'observer que ceux-cis interviennent principalement au cours de phases en .5, à savoir les phases où les cercles se referment.  

Les patterns sont similaires quel que soit le format, toutefois les kills interviennent plus tard en WWCD qu'en SUPER.

![](/files/img/phaseDeaths_FR.png)



### Rang en nombre de kills des équipes Top 1

Alors que la controverse autour du format WWCD porte entre autres sur le fait que celui-ci ne récompense pas le skill qui consiste à éliminer ses adversaires, il peut être intéressant d'étudier dans quelle mesure les équipes qui se placent 1ères d'un match sont celles qui réalisent le plus de kills.

![](/files/img/top1TeamsKillRank_FR.png)

Il apparaît que c'est majoritairement le cas pour les deux formats. Dans les deux cas, pour 90% des matchs, l'équipe qui finit Top 1 fait partie des trois équipes qui ont réalisé le plus de kills au cours du match. En revanche, les chiffres montrent qu'il est plus fréquent que l'équipe Top 1 soit celle qui a réalisé le plus de kills au format SUPER qu'au format WWCD (61% vs 54%). 

D'un autre côté il y a plus de cas en mode SUPER où l'équipe qui gagne le match est très loin d'être celle qui compte le plus de kills (dont un match où l'équipe victorieuse est au douzième rang du classement des  kills !). 

Dans tous les cas, on n'observe pas la situation citée par des détracteurs du format WWCD, d'équipes qui camperaient tout le long du match pour ne gagner qu'avec un nombre ridiculement faible de kills.



### La supériorité numérique

La supériorité numérique est un grand classique des stratégies guerrières. Regardons comment cela s'est traduit dans PUBG au cours des PGI.S.



#### Pour les équipes qui ont fait Top 1

![](/files/img/phaseTeammatesAliveTop1_FR.png)

- Il y a systématiquement plus d'équipes qui ont gagné les matchs avec 4 joueurs phase par phase qu'avec 3, 2 ou 1 seul.
- Au format SUPER, aucun match n'a été remporté par une équipe ne comptant plus qu'un seul joueur avant la phase 8, ni ne comptant que 2 joueurs avant la phase 4
- Les choses sont légèrement différentes au format WWCD, où la proportion des matchs remportés par les équipes comportant 4 joueurs est plus importante. Egalement, des matchs ont été remportés par des équipes réduites à 1 ou 2 joueurs plus tôt dans le jeu (c'est particulièrement vrai pour des matches remportés par des équipes qui ne comptaient plus qu'1 joueur dès la phase 5).



#### Résultats par coéquipiers en vie

##### 4 coéquipiers 

![](/files/img/placementsPlayersAlive4_FR.png)

- Sans surprise, arriver en late game à 4 coéquipiers a permis aux équipes de prendre les meilleures places. C'est un peu moins le cas au format WWCD qu'au format SUPER, ce qui peut s'expliquer par le fait que plus d'équipes et de joueurs ont atteint le late game dans les matchs WWCD. 



##### 3 coéquipiers

![](/files/img/placementsPlayersAlive3_FR.png)

- Arriver en late game à 3 s'est avéré moins déterminant pour prendre les meilleures positions, surtout le TOP 1, surtout au format WWCD.



##### 2 coéquipiers

![](/files/img/placementsPlayersAlive2_FR.png)

- Aucune équipe ayant perdu deux joueurs avant la phase 3 n'a fini première



##### 1 coéquipier

![](/files/img/placementsPlayersAlive1_FR.png)

- Se retrouver solo en early game (voire mid game au format SUPER) a rarement donné de bons résultats. Même en late game, les solos ont plus souvent terminé 3ème que second ou premier.



### Circle Luck

Le terme *circle luck* est utilisé pour parler d'équipes qui se trouvent dans le cercle, phase après phase, sans avoir besoin de se déplacer. L'enjeu de beaucoup d'équipes consiste à parier sur l'emplacement la zone de fin pour s'y rendre au plus tôt et ainsi s'assurer de survivre le plus longtemps possible.



#### Etre dans le cercle

Nous mesurons ici pour chaque phase et pour chaque classement final, le pourcentage de cas où l'équipe était dans le cercle

![](/files/img/teamInCircle_FR.png)

- Lors de l'apparition du 1er cercle (phase 1), les équipes ne sont majoritairement pas dans le cercle. Cela semble normal car les maps sont grandes et les équipes ont tendance à choisir des drop spots éloignées les unes des autres.
- les phases en .5 présentent des chiffres plus élevés que les phases précédentes. Cela paraît logique si on considère que les cercles sont apparus en phases entières et que les équipes ont fait en sorte de prendre de bonnes positions à l'intérieur de ceux-cis avant qu'ils ne se referment. Les chiffres sont les plus élevés pour les phases 2.5, 3.5 et 4.5. Ils sont sans doute plus faibles en phase 1.5 car les équipes prennent du temps pour looter en début de match, les distances à parcourir peuvent être importantes, le cercle met du temps à se refermer en phase 1.5 et dans le pire des cas, le bleu est peu douloureux en début de match ; plus faibles également dans les phases en .5 supérieures à 5.5 car le délai pour rejoindre les cercle diminue, et que l'espace disponible à l'intérieur des cercles se faisant plus rare, cela prend plus de temps pour s'y insérer.
- Etre on non dans le 1er cercle lorsqu'il apparaît n'est pas déterminant au regard du placement final. Le taux de présence mis en regard du classement final est relativement uniforme. L'équipe Top 1 n'est pas celle qui a les chiffres les plus élevés. C'est moins le cas au fur et à mesure des phases, où les écarts se creusent et dès la phase 3 le placement final des équipes est presque toujours aligné sur leur taux de présence dans le cercle.
- Les patterns entre le format SUPER et le format WWCD sont similaires et les chiffres relativement proches.



#### Etre le plus proche du centre du cercle

Nous mesurons ici pour chaque phase, pour les équipes qui ont fait des Top 1, le pourcentage de rang en distance du centre du cercle (rang 1  = équipe la plus proche, rang 16 = équipe la plus éloignée)

![](/files/img/rankFromCircleCenterTop1_FR.png)

Traditionnellement, à chaque apparition d'un nouveau cercle, autant que possible les équipes vont tâcher de se rapprocher du centre du cercle afin de limiter la distance à parcourir pour rejoindre le cercle suivant si celui-ci s'éloigne (*hard shrink*). Souvent les équipes qui sont déjà bien placées dans le cercle ne vont pas bouger pour retarder le moment où elles vont devoir affronter les autres équipes et risquer de perdre des joueurs ou d'être éliminées.

- Lors de l'apparition du 1er cercle (phase 1), les équipes les plus proches du centre du cercle (rang 1) ont eu un léger avantage par rapport aux équipes plus éloignées. Cela reste très léger, et on peut par (contre-)exemple observer au format SUPER que les équipes au 8ème rang ont connu un nombre de cas assez proche, alors que les équipes au 3ème rang de distance présentent les plus mauvais chiffres.
- C'est à partir de la phase 7.5 qu'être le plus proche du centre du cercle semble être plus fortement corrélé avec le fait de finir Top 1.
- Les patterns entre le format SUPER et le format WWCD sont similaires et les chiffres relativement proches.



#### Etre le plus proche de la zone de fin

Contrairement à être le plus proche du centre du cercle, qui à l'exception du 1er cercle est une chose sur laquelle les équipes peuvent agir, être le plus proche de la zone de fin correspond à la part de hasard -et donc de chance- que comporte PUBG. Ne sachant pas avant la phase 8 où se trouvera la zone de fin, il faut noter que des équipes qui en étaient initialement proches peuvent s'en éloigner quand elles vont tâcher de se rapprocher du centre des premiers cercles.

Nous observons ici dans quelle mesure cette composante de hasard impacte les équipes, et surtout si elle diffère selon le format SUPER ou WWCD.

![](/files/img/rankFromEndZoneTop1_FR.png)

- Lors de l'apparition du 1er cercle (phase 1), les équipes les plus proches de la zone de fin (rang 1) ont eu un léger avantage par rapport aux équipes plus éloignées. Cet avantage a été plus important que celui consistant à être proche du centre du cercle de phase. Et surtout il s'accroît plus rapidement au fur et à mesure des phases.
- Les patterns entre le format SUPER et le format WWCD sont similaires. L'avantage paraît légèrement plus marqué au format WWCD qu'au format SUPER sur les premières phases, cette différence s'inverse sur le mid-game.



## Conclusions

### En général

L'analyse de ces données nous permet de tirer des enseignements certainement connus par expérience par les joueurs professionnels. Pour gagner un match :

- Il est préférable d'arriver à 4 en late game !
- Etre le plus proche de la zone de fin présente un avantage supérieur à celui d'être le plus proche du centre du cercle à chaque phase. Toutefois cet avantage n'est pas massif dès la première zone, donc la circle luck semble quand même résulter d'une intuition qui permet aux meilleures équipes de faire les bonnes rotations en early game.
- Les jeux ne sont pas faits dès la phase 1. En revanche, à partir de la zone 3, selon la distance d'une équipe par rapport au centre du cercle et son nombre de coéquipiers, les chances de finir Top 1 peuvent s'avérer très faibles et amener à considérer d'autres types de stratégie de jeu.



### WWCD vs. SUPER

La plupart des patterns étudiés sont similaires entre les deux formats. Les différences les plus visibles sont :

- Le format WWCD semble voir l'action se décaler vers le mid/late-game, et il semble en effet logique qu'avec un système qui récompense principalement le Top 1 les équipes essaient de retarder autant que possible le moment où elles vont devoir s'affronter.

- Les équipes victorieuses au format WWCD sont en comparaison moins souvent celles qui font le plus de kills au cours des match, ce qui a du sens étant donnée que les kills ne sont pas valorisés au même titre qu'au format SUPER. Toutefois les ordres de grandeur entre les deux formats sont respectés et on n'observe pas d'aberrations.

- Pour adresser le sujet d'un format WWCD qui favoriserait la chance, les chiffres ne témoignent pas d'une circle luck qui affecterait un format plutôt que l'autre.



### Pour aller plus loin

Des analyses plus poussées pourront être intéressantes à réaliser pour tenter d'identifier de possibles raisons de succès des équipes : rotations tôt ou tard, jouer groupés ou espacés, être agressif ou patient, quelles sont les caractéristiques des équipes qui restent à 4 coéquipiers en vie le plus longtemps...

Les tournois à venir qui mettent en place le format WWCD permettront de recueillir de nouvelles données et d'observer comment les joueurs professionnels évoluent pour s'y adapter.



> **Méthode employée**
>
> - Utilisation de l'API PUBG pour récupérer les fichiers Json des matchs :
>     - Stats : quelques stats générales consolidées à l'échelle du match par joueur (kills, assists, heals...)
>     - Telemetry : fichier qui loggue les événements ayant eu lieu au cours du match. En moyenne 40.000 événements par match allant pour chaque joueur des objets ramassés, utilisés, véhicules conduits, tirs, hits, knocks, kills, revives etc. Particulièrement sont logguées par intermittence les positions des joueurs.
> - Pour chaque match, extraction de données dans les fichiers et création d'indicateurs :
>     - Autour de chaque changement de phase, pour chaque joueur en vie, récupération des données de position
>     - Calcul des distances entre les positions des coéquipiers
>     - Calcul du barycentre des positions des coéquipiers pour définir une position de l'équipe
>     - Mesure de la distance séparant la position de l'équipe du centre du cercle ainsi que de la zone finale. Classement des équipes selon leurs distances respectives.
>     - Selon le rayon des cercles, calcul de la présence de la position de l'équipe dans le cercle
> - Data mining et dataviz (python)