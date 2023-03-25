**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

<h1>
  Go <img src="./assets/go.svg" width="40" height="40" />
</h1>

<h2>Most Popular Go Interview Questions and Answers</h2>


<details>
<summary>1. Qu'est-ce que Go et pour quelles tâches a-t-il été créé ?</summary>

#### Go

Go (ou Golang) est un langage de programmation compilé et typé statiquement créé
chez Google par Robert Griesemer, Rob Pike et Ken Thompson. Il est conçu en
mettant l'accent sur la simplicité, la prévisibilité, la compilation rapide et
les hautes performances des systèmes de production.

#### Pour quelles tâches Go a été créé :

1. **Systèmes réseau et serveur :** services HTTP/API, proxys, passerelles,
   backend pour applications à forte charge.

2. **Infrastructure cloud :** outils d'orchestration, CI/CD, observabilité,
   utilitaires DevOps (c'est pourquoi de nombreux projets cloud natifs sont
   écrits en Go).

3. **Informatique concurrente :** tâches pour lesquelles le traitement parallèle
   des données, le contrôle de la latence et l'utilisation efficace des
   ressources sont importants.

4. **Programmation système au niveau de l'application :** outils CLI, démons,
   travailleurs en arrière-plan, services d'intégration.

#### Pourquoi Go :

- Syntaxe concise et faible complexité cognitive du code.

- Modèle de concurrence intégré (`goroutine`, `channel`).

- Compilation rapide et cycle de développement simple.

- Boîte à outils standard pratique (`go test`, `go vet`, `pprof`, modules).

Par conséquent, Go a été créé comme un langage d’ingénierie pratique pour des
services évolutifs, maintenables et performants où la fiabilité, la vitesse de
développement et la simplicité opérationnelle sont importantes.

</details>


<details>
<summary>2. Quels sont les grands principes de conception du langage Go ?</summary>

#### Go

La conception de Go n'est pas basée sur une « expressivité » maximale à tout
prix, mais sur la faisabilité technique : le code doit être facile à lire,
facile à maintenir et fiable pendant le long cycle de vie du système.

#### Principes de base de la conception Go :

1. **La simplicité plutôt que la complexité :** Le langage évite délibérément
   les constructions trop complexes pour réduire le nombre d'erreurs et le seuil
   d'entrée dans la base de code.

2. **Lisibilité et absence d'ambiguïté :** Un code clair qui peut être
   rapidement compris par n'importe quel ingénieur de l'équipe, et pas seulement
   par l'auteur, est préféré.

3. **Compilation rapide et développement productif :** Le cycle "écrit →
   construit → testé" doit être court, ce qui accélère les itérations dans les
   projets réels.

4. **Concurrence intégrée :** `goroutine` et `channel` sont une partie organique
   du langage, et non un correctif externe, le calcul parallèle est donc pris en
   charge de manière native.

5. **Composition sur une hiérarchie lourde :** Go privilégie l'approche
   consistant à "composer un comportement à partir de parties simples" plutôt
   que de construire des chaînes d'héritage profondes.

6. **Minimalisme dans les fonctionnalités, maximisation dans la praticité :**
   moins de "magie", comportement plus prévisible lors de l'exécution et du
   débogage.

7. **Norme d'outillage unique :** `go fmt`, `go test`, `go mod`, `go vet`
   forment une culture de développement commune sans fragmentation des outils.

#### Généralisation :

Go est conçu comme un langage de développement d'équipe et de programmation
industrielle : il discipline le style, encourage la clarté de la pensée dans le
code et offre un bon équilibre entre simplicité et efficacité.

</details>


<details>
<summary>3. Quelles sont les principales fonctionnalités de Go par rapport aux autres langages ?</summary>

#### Go

Go se distingue par le fait qu'il combine une syntaxe concise avec un modèle
d'exécution d'ingénierie très pratique : le langage ne surcharge pas le
développeur d'une complexité inutile, mais fournit des outils pour construire
des systèmes rapides et fiables.

#### Principales fonctionnalités de Go :

1. **Syntaxe simple et stricte :** le code est facile à lire et l'uniformité
   stylistique est maintenue automatiquement via `go fmt`.

2. **Compilez en binaire natif :** une application est généralement compilée en
   un seul exécutable sans dépendances externes lourdes au démarrage.

3. **Typage statique à haute prévisibilité :** un grand nombre d'erreurs sont
   détectées au stade de la compilation, ce qui augmente la fiabilité de la
   production.

4. **Concurrence intégrée :** `goroutine` et `channel` font de la programmation
   parallèle un mécanisme naturel plutôt qu'auxiliaire.

5. **Cycle de développement rapide :** une compilation relativement rapide et
   des outils standard accélèrent les tests et la livraison des modifications.

6. **Bibliothèque standard solide :** mise en réseau, HTTP, cryptographie,
   manipulation de fichiers, profilage et tests disponibles immédiatement.

7. **Modèle d'erreur explicite :** Dans Go, les erreurs sont gérées
   explicitement via `error`, ce qui rend le contrôle d'état transparent et
   contrôlable.

8. **GC et mémoire gérée :** Le langage simplifie le développement backend du
   système sans vous obliger à gérer manuellement le cycle de vie de la plupart
   des objets.

9. **Une approche modulaire pratique :** `go mod` standardise la gestion des
   dépendances et la reproductibilité des builds.

#### Conclusion :

Contrairement à de nombreux langages qui gravitent soit vers une abstraction
maximale, soit vers une contrôlabilité de bas niveau, Go maintient délibérément
un équilibre technique : simplicité, performances, évolutivité et commodité de
développement en équipe.

</details>


<details>
<summary>4. Quelle est la différence entre le paradigme de programmation impératif et déclaratif ? Donnez des exemples de langues.</summary>

#### Go

Les paradigmes impératifs et déclaratifs diffèrent principalement par l'objet de
la description : le premier explique **comment** effectuer la tâche étape par
étape, le second — **ce qui exactement** devrait être obtenu en conséquence.

#### Paradigme impératif :

1. **Essence :** Le programmeur spécifie explicitement la séquence
   d'instructions, les transitions d'état, les boucles, les branches et l'ordre
   d'exécution.

2. **Focus :** contrôle des algorithmes et contrôle du flux d'exécution.

3. **Caractéristiques typiques :** variables, affectations, `for`, `if`,
   mutation de données.

4. **Exemples de langages :** Go, C, C++, Rust (dans la plupart des pratiques),
   Java.

#### Paradigme déclaratif :

1. **Essence :** décrit le résultat souhaité ou les propriétés du système sans
   détailler les étapes de mise en œuvre.

2. **Focus :** modèle de données, règles et contraintes, pas de mécanique
   algorithmique.

3. **Caractéristiques typiques :** expressions de niveau supérieur, minimisation
   des mutations explicites, abstraction de l'ordre d'exécution.

4. **Exemples de langages/approches :** SQL, HCL (Terraform), HTML/CSS, styles
   fonctionnels en Haskell et en partie en Elixir.

#### Conclusion pratique :

- Dans les systèmes réels, les paradigmes sont souvent combinés.

- Go est principalement de nature impérative, mais certains éléments déclaratifs
  apparaissent dans les configurations, les descriptions de schémas, les DSL et
  les requêtes de données.

- Pour l'entretien, il est important de souligner que le choix du paradigme
  n'est pas une question de "meilleur ou pire", mais une question d'adéquation à
  la tâche, à l'équipe et aux exigences de support du code.

</details>


<details>
<summary>5. Pourquoi Go est-il adapté à l'écriture de services Cloud Natifs ?</summary>

#### Go

Ce n'est pas un hasard si Go est considéré comme l'un des langages les plus
naturels pour Cloud Native : ses propriétés architecturales correspondent bien
aux exigences des systèmes distribués modernes : évolutivité, observabilité,
fiabilité et simplicité opérationnelle.

#### Pourquoi Go est efficace dans un environnement Cloud Native :

1. **Informatique concurrente légère :** `goroutine` et `channel` simplifient la
   construction de services qui gèrent simultanément un grand nombre de
   requêtes.

2. **Hautes performances et durée d'exécution prévisible :** Le compilateur Go
   et le planificateur optimisé fonctionnent bien dans les scénarios de réseau
   chargés.

3. **Démarrage et déploiement rapides :** généralement, le résultat d'une build
   est un binaire unique facile à conteneuriser et à déployer sur Kubernetes ou
   d'autres orchestrateurs.

4. **Faible surcharge opérationnelle :** Images Docker simples, construction
   rapide, moins de problèmes de dépendance au démarrage.

5. **Puissante bibliothèque standard :** `net/http`, `context`, `crypto`,
   `encoding` et d'autres packages vous permettent de créer des solutions de
   production sans dépendance excessive à l'égard de frameworks tiers.

6. **Commodité pour les praticiens de l'observabilité :** Dans Go, il est facile
   d'intégrer les métriques, le traçage et le profilage, ce qui est essentiel
   pour l'exploitation du cloud.

7. **Écosystème résistant d'outils d'infrastructure :** Une grande partie de la
   pile Cloud Native est écrite spécifiquement en Go (par exemple Kubernetes,
   Prometheus, Helm, Terraform), ce qui simplifie les intégrations et le
   contexte des commandes.

8. **Clarté du code dans le développement d'équipe :** Go encourage les
   solutions simples, ce qui réduit la charge cognitive liée à la prise en
   charge d'une architecture de microservices.

#### Résumé :

Go est bien adapté aux services Cloud Native car il combine prévisibilité
technique, performances et commodité pratique : de l'écriture du code à son
déploiement, sa surveillance et son support à long terme.

</details>


<details>
<summary>6. Que sont les variables `shadowing` et comment peuvent-elles provoquer des erreurs dans la logique métier ?</summary>

#### Go

`Shadowing` (shadowing) se produit lorsqu'une nouvelle variable est déclarée
dans la portée interne avec le même nom que la portée externe. De ce fait, le
code ne fonctionne pas avec la variable "attendue", mais avec sa copie locale
par nom.

#### Comment cela se produit le plus souvent :

1. **Déclaration courte `:=` dans un bloc imbriqué :** le développeur attend une
   affectation, et en fait une nouvelle variable est créée.

2. **La gestion des erreurs (`err`) dans `if`/`for`/`switch` :** le `err` local
   éclipse celui externe, provoquant l'échec des vérifications d'état
   ultérieures.

3. **Travailler avec l'état dans des fonctions longues :** l'ombrage des
   variables intermédiaires rend la lecture plus difficile et augmente le risque
   de défauts logiques.

#### Pourquoi cela est dangereux pour la logique métier :

1. **Vérifications de fausses conditions :** le système peut passer à la
   mauvaise branche d'exécution car la "mauvaise" variable est vérifiée.

2. **État perdu ou incorrect :** par exemple, le résultat du calcul est resté
   dans le bloc local et l'état externe n'a pas été mis à jour.

3. **Débogage complexe :** visuellement, le nom est le même, mais
   sémantiquement, ce sont des objets différents ; l'erreur se manifeste
   discrètement et souvent uniquement dans les cas de combat.

4. **Défauts discrets sans panique :** un programme peut se compiler et
   s'exécuter, mais renvoyer un résultat incorrect pour l'entreprise.

#### Comment éviter `shadowing` :

- Faites délibérément la distinction entre `=` et `:=` dans tous les blocs
  imbriqués.

- Gardez une visibilité variable courte et évitez les fonctions trop longues.

- Utilisez des noms clairs et sémantiquement précis, en particulier pour les
  états et les erreurs.

- Connectez l'analyse statique (`go vet`, `golangci-lint`) aux règles de
  détection d'ombrage.

- Dans les endroits critiques de la logique, ajoutez des tests pour les
  scénarios négatifs et les conditions aux limites.

#### Conclusion :

`Shadowing` n'est pas une bizarrerie syntaxique, mais une source d'erreurs
logiques insidieuses. Dans le code Go de production, la discipline de
déclaration des variables affecte directement l'exactitude du comportement
commercial du système.

</details>


<details>
<summary>7. Pourquoi utiliser `struct{}` (une structure vide) et dans quels scénarios est-il efficace ?</summary>

#### Go

`struct{}` dans Go est une structure vide, c'est-à-dire un type sans champ. Sa
propriété clé : il ne transporte pas de charge utile de données, mais enregistre
uniquement le fait même de l'existence d'une valeur ou d'un événement.

#### Pourquoi `struct{}` est efficace :

1. **Volume d'informations nul :** le type ne contient aucun champ, il est donc
   utilisé comme jeton et non comme conteneur de données.

2. **Sémantique d'intention claire :** le code montre explicitement que le fait
   "est/n'est pas" est important, pas la charge utile.

3. **Réduire les allocations redondantes dans les structures de service :** dans
   de nombreux modèles, il s'agit d'un choix plus pratique que `bool` ou des
   valeurs arbitraires lorsque les données ne sont pas nécessaires.

#### Scénarios d'utilisation typiques :

1. **Défini via `map[K]struct{}` :** `map` dans Go est une valeur-clé, et pour
   un ensemble, nous n'avons besoin que de clés uniques. `struct{}` signifie ici
   idéalement « clé présente ».

2. **Les canaux de signal `chan struct{}` :** sont utilisés pour la notification
   « un événement s'est produit » (arrêt/terminé/arrêt) lorsqu'aucune donnée ne
   doit être transmise.

3. **Types de jetons et contrats d'API :** Une structure vide peut agir comme un
   jeton sémantique léger dans les protocoles internes de l'application.

4. **Incorporation de composition de comportement :** `struct{}` est parfois
   utilisé comme élément technique de composition lorsqu'une structure apatride
   est requise.

#### Quand ne pas utiliser :

- Lorsque l'état ou les attributs réels d'une entité sont requis.

- Lorsque `bool` donne une sémantique commerciale plus claire (par exemple, un
  indicateur de condition explicite plutôt qu'un fait défini).

#### Résumé :

`struct{}` est un outil pour une intention précise : si des données ne sont pas
nécessaires, mais qu'un fait, une présence ou un signal doit être indiqué, une
structure vide est une solution élégante et efficace dans le code Go.

</details>


<details>
<summary>8. Comment fonctionne la structure interne `slice` et que se passe-t-il lorsque vous la transmettez à une fonction ?</summary>

#### Go

Dans Go, `slice` n'est pas le tableau lui-même, mais un descripteur «
complémentaire » léger sur une section du tableau. C'est pourquoi le
comportement de `slice` diffère de la copie normale d'un tableau et provoque
souvent des erreurs dans les entretiens et dans le code réel.

#### Modèle interne `slice` :

`slice` se compose conceptuellement de trois parties :

1. **Pointeur vers le tableau de base** (`ptr`)

2. **Longueur** (`len`) - combien d'articles sont disponibles maintenant

3. **Capacité** (`cap`) — combien d'éléments sont disponibles jusqu'à la limite
   du tableau de base

Autrement dit, `slice` stocke les métadonnées sur la région en mémoire, plutôt
que de dupliquer tous les éléments.

#### Que se passe-t-il lorsque vous transmettez `slice` à une fonction :

1. **L'en-tête `slice` (ptr/len/cap) est copié, pas l'intégralité du tableau.**

2. **Les deux parties (appelant et appelé) regardent initialement le même
   tableau de base.**

3. **La modification d'éléments via l'index** (`s[i] = ...`) dans la fonction
   est généralement visible de l'extérieur, car les données du tableau partagé
   sont modifiées.

4. **La modification de l'en-tête lui-même** (`s = s[:n]`, `s = append(...)`)
   dans une fonction ne modifie pas l'en-tête de l'appelant, sauf si vous
   renvoyez un nouveau `slice`.

#### Nuance clé avec `append` :

- S'il y a suffisamment de `cap` pendant `append`, l'entrée va au même tableau
  de base.

- Si `cap` est manquant, le runtime alloue un nouveau tableau, y copie les
  données et le `slice` local dans la fonction commence à faire référence à une
  autre mémoire.

Ainsi, après `append`, la fonction peut déjà fonctionner avec le nouveau
tableau, tandis que l'ancien `slice` restera à l'extérieur si la nouvelle valeur
n'est pas renvoyée.

#### Conclusion pratique :

- Vous souhaitez modifier des éléments - vous pouvez transmettre `slice` tel
  quel.

- Vous souhaitez modifier la longueur/capacité ou le résultat de `append` -
  renvoyez le `slice` mis à jour à partir de la fonction (ou passez un pointeur
  vers `slice` lorsque cela est vraiment justifié sur le plan architectural).

#### Exemple :

```go
package main

import "fmt"

func grow(s []int) {
	s = append(s, 99) // змінюємо локальний заголовок slice
}

func mutate(s []int) {
	s[0] = 42 // змінюємо спільний базовий масив
}

func main() {
	s := []int{1, 2, 3}
	mutate(s)
	grow(s)
	fmt.Println(s) // [42 2 3], append у grow не змінив заголовок у викликачі
}
```

</details>
