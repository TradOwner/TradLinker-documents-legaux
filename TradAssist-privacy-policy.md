**🔒 Politique de confidentialité (RGPD) - TradAssist**

Dernière mise à jour : 06/10/2025

**1. Données traitées**

*a. Données Discord (usage courant)*
- Identifiants techniques : ID utilisateur/serveur/canal/message, rôles/permissions nécessaires au bon fonctionnement.
- Contenu des messages (texte) pour réaliser la traduction et renvoyer le résultat. Le Bot segmente et prépare le texte en conservant les éléments non traduisibles (URLs, mentions, code) et peut convertir des mentions textuelles en mentions <@id> lorsqu’autorisé. 
- Fichiers/émojis/stickers : éventuellement relayés pour l’affichage, sans extraction de contenu non nécessaire. 

*b. Mesure d’usage et limites*
- Compteurs mensuels par serveur/utilisateur/fonction enregistrés dans usage.json, avec synchronisation périodique (environ toutes les heures si modifié) vers un dépôt GitHub privé. 

*c. Abonnements Platinium (paiements Stripe)*
- Mapping Stripe : stripe_users.json contient pour chaque user_id Discord un customer_id et un subscription_id Stripe. 
- Liste des abonnés : platinium_users.json liste les user_id actifs. Ces deux fichiers peuvent être poussés/synchronisés vers un dépôt GitHub privé. 

**2. Origine des données**
- Discord (messages et métadonnées nécessaires au traitement).
- Stripe (webhooks d’événements d’abonnement/résiliation). 

**3. Finalités et bases légales (art. 6 RGPD)**
- Fourniture du service de traduction : exécution d’un contrat (acceptation des CGU).
- Gestion des quotas : intérêt légitime (protéger le service).
- Facturation des abonnements : exécution du contrat et obligations légales (comptabilité).
- Sécurité / sauvegarde (synchronisation GitHub privé) : intérêt légitime. 

**4. Destinataires – Sous-traitants**
- Discord (plateforme).
- API pour la traduction (ex: DeepL, Microsoft, Google). 
- Stripe pour les paiements (gestion des clients/abonnements). 
- GitHub (dépôt privé pour sauvegarde/restore de certains fichiers). 
- Hébergeur du serveur du Bot et de l’API (FastAPI) recevant les webhooks Stripe (pages /success, /cancel, /webhook). 

**5. Durées de conservation**
- Contenu de messages à traduire : traité à la volée et non conservé au-delà du temps nécessaire à la réponse.
- Compteurs d’usage (usage.json) : 1 mois glissants.
- Liste abonnés (platinium_users.json) : pendant l’abonnement.
- Mapping Stripe (stripe_users.json) : tant que le compte Stripe du client existe + durée légale applicable (comptable/fiscale).
- Les sauvegardes GitHub privées suivent les mêmes durées (avec effacement sur demande justifiée). 

**6. Sécurité**
- Communications chiffrées avec les APIs tierces (Discord/Stripe/APIs/GitHub).
- Accès restreint par jetons d’API (GitHub/Stripe). Le dépôt GitHub utilisé est privé. 
- Journalisation minimale et principe de minimisation des données.

**7. Vos droits**
- Conformément au RGPD : droit d’accès, de rectification, d’effacement, d’opposition, à la limitation, à la portabilité, et directives post-mortem. Pour exercer vos droits : tradsphere@gmail.com.
- Vous pouvez également saisir l’autorité de contrôle compétente (CNIL en France).

**8. Paiements**
- Les paiements sont traités par Stripe. Nous ne stockons pas de données de carte ; nous recevons uniquement des identifiants techniques (client/abonnement) et des webhooks nécessaires à l’activation/suspension de l’accès Platinium. 

**9. Enfants**
- Le service n’est pas destiné aux personnes ne remplissant pas l’âge requis par Discord.

**10. Modifications**
- Nous pouvons modifier la présente politique ; la date de « Dernière mise à jour » sera ajustée. En cas de changement substantiel, une information raisonnable sera fournie via Discord ou la documentation du Bot.

**11. Contact**
- Pour toute question ou demande concernant la confidentialité, contactez-nous via le serveur support : [Support TradSphere](https://discord.gg/c5zvbAWwu8)
