
  **Description des Exigences du Système**

 L'application à concevoir est un système de gestion de commandes de repas en ligne destiné à un restaurant de type Fast-Food. Le système interagit principalement avec deux types d'utilisateurs : le Gérant du restaurant et les Clients.

 Du côté du **Gérant**, le système doit lui offrir une interface lui permettant de gérer son catalogue en ayant la possibilité d'ajouter de nouveaux plats au menu (avec leur nom, prix, et description). Au quotidien, le gérant utilise l'application pour lister toutes les commandes actuellement en attente. Lorsqu'une nouvelle commande est reçue, il a la responsabilité de la valider manuellement. Une fois la commande prête, le système lui permet d'assigner un livreur spécifique qui sera chargé d'acheminer le repas au client.

 Du côté du **Client**, l'utilisateur peut se connecter à la plateforme pour consulter le menu complet des plats proposés par le restaurant. S'il trouve ce qu'il désire, il peut passer une commande en ajoutant des plats à son panier. Le système doit lui permettre de payer sa commande directement en ligne par carte bancaire. Enfin, le client dispose d'un espace personnel où il peut consulter l'historique détaillé de toutes ses commandes précédentes.

 *Livrables Attendus (UML)*
   **1- Diagramme des Cas d'Utilisation (Use Case)** 
        * À partir du texte ci-dessus, identifier et représenter les acteurs (Client, Gérant, Système Bancaire, Livreur).
        * Modéliser les cas d'utilisation extraits de la description avec les relations appropriées (include, extend, généralisation).
   
   **2- Diagramme de Classes d'Analyse**     
        * Identifier les entités métiers du domaine 
        * Définir les associations sémantiques entre ces entités, les multiplicités et les rôles, sans se préoccuper des méthodes ou de la typologie technique détaillée.
        
   **3- Diagrammes de Séquence**
        Modéliser le flux temporel des messages pour les 4 scénarios suivants :
        
        *Scénario 1 : "Passer une Commande"*
            *RG1 : Le client sélectionne un ou plusieurs plats à ajouter à son panier.*
            *RG2 : Le système vérifie la disponibilité de chaque plat.*
            *RG3 : Le système calcule le montant total de la commande.*
            *RG4 : Le client valide la commande et le système l'enregistre avec le statut "En attente".*
            
        *Scénario 2 : "Payer une Commande en ligne"*
            *RG1 : Le client choisit de payer une commande "En attente".*
            *RG2 : Le système transmet les informations de paiement au Système Bancaire.*
            *RG3 : Le Système Bancaire valide la transaction et renvoie une confirmation.*
            *RG4 : Le système met à jour la commande au statut "Payée" et génère un reçu pour le client.*
            
        *Scénario 3 : "Valider une Commande entrante"*
            *RG1 : Le gérant sélectionne une commande ayant le statut "Payée".*
            *RG2 : Le gérant confirme le lancement de la préparation en cuisine.*
            *RG3 : Le système met à jour la commande au statut "En préparation".*
            *RG4 : Le système envoie automatiquement une notification au client pour l'informer.*
            
        *Scénario 4 : "Assigner un Livreur"*
            *RG1 : Le gérant sélectionne une commande prête à être expédiée.*
            *RG2 : Le système lui affiche la liste des livreurs actuellement "Disponibles".*
            *RG3 : Le gérant sélectionne un livreur et valide l'assignation.*
            *RG4 : Le statut de la commande passe à "En livraison", le livreur devient "Occupé", et une notification d'assignation lui est envoyée.*
            



