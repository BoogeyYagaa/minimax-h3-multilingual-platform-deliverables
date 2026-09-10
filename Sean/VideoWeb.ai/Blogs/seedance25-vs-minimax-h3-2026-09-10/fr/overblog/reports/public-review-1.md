verdict: PUBLIC_REVIEW_CHANGES

# FR-01 — revue publique anonyme R-P 1

## Portée, URL et empreintes

- **URL publique lue :** `https://videowebai.overblog.fr/2026/09/seedance-2.5-vs-minimax-h3-ecrire-le-brief-d-une-courte-video-de-chambre.html`
- **Collecte :** 2026-09-10T08:37:58.285Z, lecture HTTPS anonyme et strictement non mutante.
- **Preuve publique :** `evidence/public-rp-1.md`.
- **HTML public :** SHA-256 `51b417c5b176fd3388e779bb2e15d43160ff543f7fcb131e61eef61f9d55d73e`; zone article HTML `12c5994b6077e8d9ea640ae23ae9639f527a9bc026109103d6c525c9852a8d45`; texte normalisé `bf5959cde29e4530241682882e106edc16c40b24a0076e5b7c73f826de856052`.
- **Empreinte locale gelée :** canonical Markdown `ac3e1f3ec4408200c005e69392563df535df176c840ab66864a05b6db6ebb391`; canonical HTML `c24e7d69ee2056411d80e1514f06a36bfb326cf030ef872a96d024881f5c0a93`; visual payload `f89c7bd1f78e270ca3500a1ea45ff81db2f61ee415dfebdc4dc86e0ba4967a29`.

La revue relit le contrat local, les rapports R/G locaux jusqu’à `r3/gate-report-1.md`, le canonical, le paquet Overblog et son fingerprint. Elle ne transforme ni `HUMAN_RELEASE_READY`, ni l’URL, ni HTTP 200 en publication acceptée. Aucun navigateur avec profil, compte, connexion, éditeur ou écriture de plateforme n’a été utilisé.

## Résultats indépendants

| Finding ID | Statut | Preuve et résultat |
|---|---|---|
| PUBLIC-RENDER-001 | OPEN | Les deux URL gelées doivent chacune figurer une fois, avec leurs ancres descriptives. Dans le HTML public complet, les deux libellés sont visibles mais sont des `<span>` sans lien ; `https://videoweb.ai/model/seedance-2-5/` = 0 et `https://videoweb.ai/model/minimax-h3/` = 0. Aucun href VideoWeb n’est présent dans le corps public. Preuve : `evidence/public-rp-1.md`, comparaison à `human-release/overblog/links.md` et `fingerprint.json`. **Réparation minimale humaine :** rétablir ces deux ancres avec les href exacts, une occurrence chacun, dans le premier paragraphe du premier H2 ; ne pas modifier les textes d’ancre ni ajouter d’autre lien VideoWeb. |
| PUBLIC-RENDER-002 | OPEN | Le H1 public et les six H2 correspondent au canonical, mais le DOM public contient 0 `<h3>`. Les trois intertitres gelés (`Ce que ce comparatif ne peut pas établir`, `Version centrée sur la scène`, `Version centrée sur le trajet de la caméra`) sont des `<div class="ob-h3">`, au lieu de H3. Cela ne préserve pas la structure lecteur H1/H2/H3 exigée. Preuve : `evidence/public-rp-1.md`; référence locale : `fingerprint.json:heading_transport`. **Réparation minimale humaine :** restaurer ces trois intertitres comme H3 sémantiques, sans changer leur texte, leur ordre, le reste du corps ou les images. |
| PUBLIC-RENDER-003 | PASS | Le public est anonymement accessible, `lang="fr"`, H1 exact et six H2 dans l’ordre. Tous les 38 segments textuels du canonical (H1 séparé puis 37 segments de zone article) sont retrouvés dans l’ordre ; aucune carte chinoise ou texte d’insertion n’apparaît. La disclosure founder et la limite « pas de test indépendant » sont présentes. |
| PUBLIC-RENDER-004 | PASS | Trois figures publiques sont présentes aux emplacements LEAD/MIDDLE/CLOSING attendus avec les trois ALT et légendes gelés, dans le bon ordre. Leurs `src` répondent chacun HTTP 200 `image/png`. Les vérifications concernent DOM et disponibilité de ressources ; aucune identité de hash binaire publique ni capture visuelle n’est revendiquée. |
| PUBLIC-RENDER-005 | PASS | Métadonnées réellement accessibles : title public avec suffixe de site, description publique tronquée, `robots=index,follow` et canonical public égal à l’URL lue. Cela constate l’état rendu seulement ; il ne prouve pas de support Overblog des champs natifs locaux, qui reste `UNVERIFIED`. |
| PUBLIC-RENDER-006 | UNVERIFIED | Aucun `HUMAN_ACCEPTED` ni `HUMAN_NEEDS_FIX` explicite n’a été fourni. L’URL publique, HTTP 200, les assets ou ce rapport ne valent pas acceptation humaine. |

## Capture et limites

La preuve détaillée est `evidence/public-rp-1.md`. Aucune capture d’écran n’existe : le navigateur intégré anonyme était indisponible et le lecteur web sûr a refusé l’ouverture de cette URL. La décision ci-dessus repose donc sur le HTML public complet et des requêtes `HEAD` d’images, non sur une supposition de rendu éditeur.

## Décision et condition de passage

`PUBLIC_REVIEW_CHANGES` est requis, exclusivement pour `PUBLIC-RENDER-001` et `PUBLIC-RENDER-002`. Une personne doit appliquer les deux corrections minimales dans l’éditeur natif, puis retourner la même URL pour une **nouvelle R-P anonyme**. Ensuite seulement, un nouveau G-P peut confronter la R-P fraîche à une décision humaine explicite. Aucun statut de publication, de compte, de runtime ou d’acceptation humaine n’est déclaré par cette revue.
