# Instructions d'installation

1. [Télécharger la version modifiée de `tarteaucitron.js`](https://github.com/Webmecanik/tarteaucitron.js/releases/latest)

2. Décompresser le zip téléchargé

3. Envoyer le dossier `tarteaucitron.js` sur votre site

4. Ajouter `<script src="tarteaucitron.js/tarteaucitron.js"></script>` sur votre site

5. Configurer `tarteaucitron.js`:
  ```html
  <script>
      tarteaucitron.job = ['automation']
      tarteaucitron.user.automationPrefix = 'demo' // pour demo.automation.webmecanik.com
      // tarteaucitron.user.automationCustomParameters = ...
      // tarteaucitron.user.automationLoadEvent = ...
      // tarteaucitron.user.automationErrorEvent = ...
      tarteaucitron.init({orientation: 'bottom'}) // pour afficher le bandeau en bas
  </script>
  ```

Vous trouverez un fichier `exemple.html` dans ce projet.

Pour plus d'informations, rendez-vous sur https://opt-out.ferank.eu/fr/install/
