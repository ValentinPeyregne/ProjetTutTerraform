#PROJET TUT - TERRAFORM 

###INTRO - DESCRIPTIF DES TÂCHES 
- Découvrir et comprendre ce qu’est le “cloud” et le IIAS
- Utiliser le client python-nova pour gérer quelques machines sur openstack (3 ou 4)
- Découvrir et se familiariser avec terraform, comprendre son utilité
- Créer un cluster de machine géré par terraform sur un unique provider (ovh)
- Procéder facilement à des opérations de gestion quotidienne (snapshots, bootstraping)

###I. DOCUMENTATION OpenStack

OpenStack est un projet qui a débuté en 2010 (licence Apache 2.0) pour monter une infrastucture dans le domaine du cloud computing.
OpenStack permet de faire du IaaS.
**IaaS** - *Infrastucture As a Service* : : Le but est d’offrir un service de bas niveau, le consommateur peut alors choisir le système d’exploitation et y installer les outils adaptés à ses besoins. Il est possible de louer dynamiquement des machines virtuelles pour une courte durée, mais il est également possible de louer un ensemble de machines constituant une infrastructure externe. Les acteurs français du IaaS sont Online.net, OVH (Kimsufi), . . .

####Les modules : services d'OpenStack :
Le développement d’OpenStack est découpé en différents modules (projets). 
Les modules sont des agrégats de multiples technologies communicant
ensemble par le biais d’interface de programmation (API) et du protocole HTTP. Ils sont par ailleurs tous indispensables pour arriver au web élastique.

##### Keystone, le service d'identité

 	

Fournit un service d’authentification et d’autorisation pour les autres services d’OpenStack. Fournit un catalogue de endpoints pour tous les services d’OpenStack.



##### Glance, la gestion d'images

Stocke et récupère des images disques de machines virtuelles. OpenStack Compute les utilise lors du provisioning d’instance.



##### Nova, le Compute

Gère le cycle de vie des instances dans un environnement OpenStack. Les tâches incluent la planification, la création et la mise hors service de machines virtuelles à la demande.



##### Horizon, l'interface web

Fournit un portail libre-service de type web permettant d’interagir avec les services sous-jacents d’OpenStack, comme le lancement d’une instance, l’attribution d’adresses IP ou la configuration des contrôles d’accès.


##### Cinder, le service de disques persistants

Fournit un stockage bloc persistant aux instances en cours d’exécution. Son architecture basée sur des drivers de type plugin facilite la création et la gestion des devices de stockage bloc.

##### Neutron, la gestion de réseaux


Permet le Network-Connectivity-as-a-Service pour d’autres services d’OpenStack, comme Compute. Fournit une API utilisateur pour définir les réseaux et les attachements à ces réseaux. Possède une architecture modulaire qui permet le support de la plupart des fournisseurs et des technologies réseau.

##### Swift, le stockage d'objet

Stocke et récupère des objets de données non structurées via une API RESTful basée sur HTTP. Le service est hautement tolérant aux pannes avec sa réplication de données et son architecture de type scale-out. Son implémentation diffère des serveurs de fichiers à répertoires montables. Le service écrit les objets et les fichiers vers plusieurs disques, en s’assurant que les données sont répliquées sur un cluster de serveurs.

##### Heat, le service d'orchestration	

Orchestre de nombreuses applications de cloud composites en utilisant soit le format de template natif HOT ou le format CloudFormation d’AWS, soit au travers d’une API REST native OpenStack, soit au travers d’une API compatible avec CloudFormation.

##### Ceilometer, le service de métrologie	

Surveille et mesure un cloud OpenStack dans un but de facturation, de mesure de performances, de scalabilité et de statistiques.


###LIENS 

https://members.loria.fr/LNussbaum/ptasrall2017/rapport_g_openstack2014.pdf

https://www.ekino.com/quelques-heures-avec-terraform-outiller-le-provisioning-amazon-web-services/

https://www.terraform.io/docs/index.html

http://blog.wescale.fr/2016/06/30/ansible-packer-terraform-un-trio-gagnant/