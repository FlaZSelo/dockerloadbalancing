# dockerloadbalancing

/!\ AFFICHER CE CONTENUE EN RAW /!\
maquette infrastructure d'équilibrage de charge docker


Ce projet a pour but de testé une structure d'équilibrage de charge sous docker.
L'arborescence ce fait à partir de mon dossier dockerloadbalacing.

Dans ce dossier parent, nous avons à la racine mon docker-compose.yml qui va servir de point 
de construction de mes containers. Dans dockerloadbalacing ce trouve un sous dossier haproxy
qui contient mon fichier de configuration haproxy ainsi que le dockerfile de mon image haproxy.

L'arborescence est donc:

dockerloadbalancing------docker-compose.yml
                       |
                       |
                       --/haproxy/--------------dockerfile
                                              |
                                              |
                                              --haproxy.cfg
                                              

Pour testé l'infra:

  - Lancé le docker-compose --> docker-compose up --build
      Lors du build des container vérifier qu'il n'y a pas d'erreur de communication avec les 2 serveurs web.
  - une fois lancé vérifier que tous vos container sont lancé avec un docker ps
  - On peut maintenant testé le services web en ouvrant dnas notre naviguateur une page web avec l'adresse IP de votre
  machine hôte. En rechargant la page vous pouvez voir que l'équilibrage de charge ce fait en swapant de serveur web.
  
  
