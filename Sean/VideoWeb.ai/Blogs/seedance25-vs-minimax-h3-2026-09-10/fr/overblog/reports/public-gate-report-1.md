verdict: PUBLIC_QA_CHANGES

# FR-01 — G-P public indépendant, tour 1

## Périmètre et indépendance

G-P a relu uniquement les artefacts persistés suivants : le contrat de campagne et sa confirmation, `assignment.json`, `lane-status.json`, le canonical, le paquet de remise Overblog (`fingerprint.json`, `visual-payload.html`, `links.md`, `image-manifest.md`, `RELEASE-CARD.md`), le G local, R-P 1 et sa preuve publique. Aucune histoire de session d’agent, aucun compte, navigateur connecté, éditeur, téléversement, modification, publication ou retrait n’a été consulté ou utilisé.

Le contrat gelé exige deux URL VideoWeb inchangées avec ancres descriptives, la divulgation founder, le paquet de trois images et la remise humaine suivie d’une validation publique. Le fingerprint fixe le titre/H1, six H2, trois H3 sémantiques et les deux liens exacts. Le G local `r3/gate-report-1.md` est seulement un `HUMAN_RELEASE_READY` local : il ne vaut ni acceptation humaine ni QA publique.

## Preuve publique actuelle et suffissance de R-P

- R-P 1 a analysé le HTML public complet de 143107 octets, isolé la zone article (SHA-256 `12c5994b6077e8d9ea640ae23ae9639f527a9bc026109103d6c525c9852a8d45`) et comparé ses 37 segments canoniques après H1, dans l’ordre, ainsi que le H1 séparé. Son SHA-256 de texte normalisé est `bf5959cde29e4530241682882e106edc16c40b24a0076e5b7c73f826de856052`.
- Relecture anonyme et non mutante par G-P à `2026-09-10T08:44:14Z` : HTTP 200, `content-type: text/html; charset=UTF-8`, document complet SHA-256 `51b417c5b176fd3388e779bb2e15d43160ff543f7fcb131e61eef61f9d55d73e`. Il est identique au HTML analysé par R-P 1 ; les deux chaînes href VideoWeb requises y comptent encore zéro occurrence. Cette concordance rend la preuve R-P actuelle, sans confondre HTTP 200 avec une réussite QA.
- R-P a suffisamment comparé le texte, l’ordre, H1/H2/H3, les deux liens, le CTA/disclosure, les trois figures, leurs ALT/légendes/positions et l’absence de cartes chinoises. Les trois ressources image étaient des PNG accessibles par HEAD HTTP 200. L’absence de capture écran ne réduit pas cette preuve : le HTML complet, les attributs DOM et les réponses de ressources sont conservés et plus probants pour ces contrôles.
- Les métadonnées publiquement observables ont aussi été lues : `lang="fr"`, titre avec suffixe Overblog, description tronquée, `robots=index,follow` et canonical égal à l’URL lue. Ce sont des observations de rendu ; le paquet ne prouve pas que les champs natifs Overblog de métadonnées soient supportés. Aucun écart public supplémentaire ne peut être déduit de cette limite de plateforme.

## Findings publics

| ID | Statut G-P | Décision fondée sur la preuve |
|---|---|---|
| `PUBLIC-RENDER-001` | OPEN | Les deux textes d’ancre français sont visibles, mais les href exacts `https://videoweb.ai/model/seedance-2-5/` et `https://videoweb.ai/model/minimax-h3/` sont absents (compte 0 chacun) ; R-P les observe comme contenu non cliquable. Cela contredit `links.md`, `fingerprint.json` et `REQ-LINK-001`. |
| `PUBLIC-RENDER-002` | OPEN | R-P établit dans la zone article 0 `<h3>` : `Ce que ce comparatif ne peut pas établir`, `Version centrée sur la scène` et `Version centrée sur le trajet de la caméra` sont des `div.ob-h3`, pas des H3 sémantiques. Cela contredit le `SEPARATE_TITLE_FIELD` et la map H2/H3 gelés. |
| `PUBLIC-RENDER-003` | PASS | Le H1 exact, les six H2, les 38 segments canoniques, leur ordre, la divulgation founder et la limite de non-test indépendant sont présents ; aucune carte d’insertion ne fuit dans le contenu lecteur. |
| `PUBLIC-RENDER-004` | PASS | Les trois figures LEAD/MIDDLE/CLOSING, les trois ALT et légendes gelés et leurs ressources PNG publiquement disponibles correspondent à la preuve R-P. Aucune identité binaire publique ou apparence au-delà du DOM n’est prétendue. |
| `PUBLIC-RENDER-005` | PASS (observation) | Le titre public, la description visible, `robots` et canonical ont été inspectés. Le suffixe et la description tronquée sont consignés comme comportement rendu/plateforme, non comme preuve d’un champ SEO natif ni comme conformité implicite d’un champ non gelé. |
| `PUBLIC-RENDER-006` | UNVERIFIED | Aucun signal explicite `HUMAN_ACCEPTED` ou `HUMAN_NEEDS_FIX` n’est fourni. Une URL, HTTP 200, le HTML, les images, R-P et le présent Gate ne peuvent pas établir l’acceptation humaine. |

## Décision et carte humaine minimale

`PUBLIC_QA_CHANGES` est requis : les deux findings ouverts sont des écarts publiquement visibles et réparables, et `HUMAN_ACCEPTED` reste `UNVERIFIED`.

Pour une personne dans l’éditeur Overblog uniquement :

1. Restaurer une seule fois chacun les deux mêmes textes d’ancre dans le premier paragraphe du premier H2, avec exactement les deux href gelés ; ne pas changer les libellés ni ajouter un autre lien VideoWeb.
2. Rétablir les trois intertitres nommés ci-dessus comme véritables H3, sans changer texte, ordre, images, ALT, légendes, title, contenu ni disclosure.
3. Retourner l’URL identique avec un résultat humain explicite : `HUMAN_ACCEPTED` si la personne accepte la page corrigée, sinon `HUMAN_NEEDS_FIX` avec les seules lignes échouées.

Après toute correction, il faut une nouvelle capture anonyme de la page, R-P frais par le reviewer FR-01, puis un nouveau G-P fresh. Cette décision n’autorise aucune modification automatique, publication, suppression ou rollback, et ne compte pas cette publication comme achevée.
