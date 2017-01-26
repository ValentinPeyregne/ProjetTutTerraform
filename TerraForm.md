## Introduction a TerraForm 

### 1. Qu'est-ce que Terraform?

Tout d'abord TerraForm est un outil pour la construction d'infrastucture  , la modification et le versioning de maniére sûre et efficace. Il permet de gérer plusieur fournisseur de services existant ainsi que les soluctions qui sont developper en interne 

TerraForm fonctionne avec des fichiers de configuration , ces fichier sont des fichiers texte qui servent a décrire l'infrastructure et définir des variables , il y a deux type de fichier .tf et .tf.json le format JSON est destiné aux machines. C'est fichiers de configuration décrivent les composants qui seront necessaire a l'exécutions de TerraForm en une seule application ou sur l'ensemble. TerraForm génère un plan d'éxécution décrivant les étapes qu'il va faire pour atteindre l'eétat désiré, puis exécute le plan.TerraForm peut aussi détecter ce qui a changé et créer des nouveau plan d'exécution.

TerraForm permet de gérer les composants de bas niveau , comme les instances de calcul , le stockage et la mise a niveau, ainsi que des composants haut niveau comme les entrées DNS , les fonctionnalités SaaS 

### 2. Caractéristiques de TerraForm 

Les principales caractéristiques de TerraForm sont : 

-** Codé sont infrastucture : ** L'infrastructure est décrit en utilisant une syntaxe de configuration de haut niveau. Cela permet à un datacenter d'être versionné et traité comme tout autre code.

-** Plans d'exécution : ** Terraform a une étape de «planification» où elle génère un plan d'exécution. Le plan d'exécution montre ce que TerraForm fera lorsque qu'il sera lancée.Cela permet d'augmenter la sécurité en evitant d'avoir des surprises lorsque TerraForm manipule l'infrastructure.

-** Graphique Resource : ** Terraform construit un graphique de toutes vos ressources, et parallélise la création et la modification de toutes les ressources non-dépendantes. Grâce a ça, TerraForm construit l'infrastructure aussi effacement que possible , et les utilisateur peuvent avoir un aperçu des dépendances dans leur infrastructure.

-** Automatisation des changements : ** Des ensembles complexes de changements peuvent être appliqués à votre infrastructure avec une interaction humaine minimale. Avec le plan d'exécution et le graphique de ressources mentionnés précédemment, vous savez exactement ce que Terraform va changer et dans quel ordre, en évitant de nombreuses erreurs humaines possibles

### 3. Quelque cas d'utilisation de TerraForm 

- Self-Service Clusters

À une certaine taille d'organisation, il devient très difficile pour une équipe d'opérations centralisées de gérer une infrastructure de grande taille et en pleine croissance. Il devient plus attrayant de créer une infrastructure «self-service», permettant aux équipes de gérer leur propre infrastructure à l'aide de l'outillage fourni par l'équipe centrale d'exploitation. 


À l'aide de Terraform, de la connaissance de la construction d'infrastructure et de l'échelle d'un service peut être codifiée dans une configuration. La configurations de Terraform peuvent être partagées au sein d'une organisation permettant aux équipes des clients à utiliser la configuration comme une boîte noire et d'utiliser Terraform comme un outil pour gérer leurs services.

- Démos de logiciels

Les logiciel sont de plus en plus en réseau et distribué. Bien que les outils comme Vagrant existent pour construire des environnements virtualisés pour les démos, il est encore très difficile de faire la démonstration du logiciel sur une véritable infrastructure qui correspond plus étroitement aux environnements de production.


Les éditeurs de logiciels peuvent fournir une configuration Terraform pour créer, fournir et démarrer une démo sur des fournisseurs de cloud comme AWS. Cela permet aux utilisateurs finaux de démo de deployé facilement leur logiciel sur leur propre infrastructure, et permet même de modifier les paramètres comme la taille du cluster pour tester plus rigoureusement les outils à toute échelles 

- Multi Cloud-Déploiement

Il est souvent attrayant de répandre l'infrastructure sur plusieurs cloud ​​pour augmenter la tolérance aux pannes. En utilisant une seule région ou un seul fournisseur cloud , la tolérance aux pannes est limitée par la disponibilité de ce fournisseur. Avoir un déploiement multi-cloud permet une meilleur récupération de la perte d'une région ou tout le fournisseur.

La réalisation des déploiements multi-cloud peut être trés difficile car de nombreux outils existent pour la gestion de l'infrastructure qui sont spécifiques aux fournisseurs du cloud. Terraform est un cloud qui permet une configuratio unique pour gérer plusieur fournisseurs , et même gérer les dépendances entre cloud. Cela simplifie la gestion et l'orchestration , en aidant les opérateurs à construire à grande échelle des infrastructures multi-cloud.




