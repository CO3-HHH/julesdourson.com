# Jules Dourson — Site professionnel V2

Site statique, **4 langues**, gratuit à héberger sur GitHub Pages. Aucune compilation ni dépendance.

## Aperçu en local

Ouvrir `fr/index.html` dans un navigateur (les liens relatifs sont conçus pour fonctionner depuis le dossier), ou servir ce dossier :

```bash
python -m http.server 8000
```

Puis ouvrir http://localhost:8000/. La racine choisit la langue à partir du navigateur (FR, EN, ES, PT), sauf si le visiteur a choisi explicitement une langue. Le choix explicite est mémorisé dans le navigateur.

## Publier sur le dépôt que tu as créé

**Dépôt :** https://github.com/CO3-HHH/julesdourson.com

**Option sans terminal :** décompresser le ZIP, ouvrir le dépôt dans GitHub > Add file > Upload files; déposer **tout le contenu du dossier** (index.html, CNAME, .nojekyll, robots.txt, sitemap.xml, dossiers fr/, en/, es/, pt/, assets/). Valider le commit. Vérifier que les dossiers ne sont pas imbriqués sous `julesdourson-site-v2/`.

**Option terminal** (si Git est installé, dépôt vide ou propre):

```bash
git clone https://github.com/CO3-HHH/julesdourson.com.git
# Copier le CONTENU de ce dossier dans le répertoire cloné.
cd julesdourson.com
git add .
git commit -m "Create multilingual consulting website V2"
git push origin main
```

Puis GitHub > dépôt > Settings > Pages > Build and deployment > Deploy from a branch > Branch `main` / `(root)` > Save.

## GoDaddy / domaine

Le domaine canonique de ce projet est `julesdourson.com` et le fichier `CNAME` le déclare.

1. **D'abord** dans GitHub > Settings > Pages > Custom domain : `julesdourson.com` (Save). L'étape de vérification de domaine GitHub est également conseillée pour limiter les risques de détournement.
2. Dans GoDaddy, ouvrir la zone DNS du domaine et vérifier les enregistrements existants, en particulier s'il y a un site web ou une messagerie déjà en service.
3. Pour le nom `@`, configurer uniquement ces quatre `A` GitHub Pages :
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. Pour `www`, ajouter un `CNAME` vers **`CO3-HHH.github.io`** (et non vers l'adresse du dépôt GitHub ni vers le sous-chemin du projet). GitHub fera normalement rediriger `www` vers le domaine canonique.
5. Après propagation, vérifier `https://julesdourson.com/fr/`, les autres langues et activer **Enforce HTTPS** dans les réglages Pages dès que l'option est disponible.
6. Ne pas supprimer les enregistrements MX/TXT utiles à une éventuelle messagerie. Supprimer seulement les conflits DNS du site web, après vérification.

**Documentation officielle :** https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Les photos et le logo

- `assets/images/jules-portrait.webp` : portrait récent, accueil.
- `assets/images/jules-naturel.webp` : portrait plus informel, section « À propos ».
- `assets/images/jules-tedx.webp` : archive TEDx.
- `assets/mark.svg` et `assets/favicon.svg` : symbole vectoriel provisoire conçu pour le site. Il représente trois forces reliées. **Le logo personnel de référence n'étant pas fourni, ce n'est pas une adaptation de celui-ci.**
- `assets/industrie-schema.svg` : illustration schématique (pas de photo documentaire générée ni de machine attribuée au client).

## Calendly

Tous les boutons d'échange ouvrent https://calendly.com/julesdourson dans un nouvel onglet. Ce choix évite le poids et les cookies d'une intégration Calendly complète. Vérifier que la page Calendly est active et que les créneaux conviennent aux visiteurs internationaux.

## Traductions

Les textes des quatre langues sont réellement intégrés dans `fr/`, `en/`, `es/` et `pt/`. Ils sont éditables indépendamment. Les versions sont actuellement de bonnes premières traductions, mais devraient être relues par Jules avant une publication officielle dans chacune des langues. FR est la version éditoriale de référence.

## À finaliser avant publication

- Relire les quatre versions, notamment promesses de service et termes d'IA.
- Confirmer le bon lien LinkedIn et la configuration de Calendly.
- Vérifier accord de confidentialité pour étude de cas anonyme.
- Ajouter une adresse de courriel professionnelle si souhaité.
- Vérifier licences de publication des photos et le lien TEDx.
