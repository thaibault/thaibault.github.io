<!-- !/usr/bin/env markdown
-*- coding: utf-8 -*-
region header
Copyright Torben Sickert (info["~at~"]tsickert.com) 16.12.2012

License
-------

This library written by Torben Sickert stands under a creative commons naming
4.0 international license.
See https://creativecommons.org/licenses/by/4.0/deed.de
endregion -->

<!--|deDE:Projektstatus-->
<!--|frFR:État du projet-->
Project status
--------------

[![deploy website](https://img.shields.io/github/actions/workflow/status/thaibault/website/deploy-website.yaml?label=deploy%20website&style=for-the-badge)](https://github.com/thaibault/website/actions/workflows/deploy-website.yaml)
[![website](https://img.shields.io/website-up-down-green-red/https/tsickert.com.svg?label=website&style=for-the-badge)](https://tsickert.com)

<!--|deDE:Einsatzmöglichkeiten-->
<!--|frFR:Cas d'utilisation-->
Use case
--------

This repository holds the built and optimized version of my personal website
[tsickert.com](https://tsickert.com), served via GitHub Pages. Nothing in
here is hidden on purpose, everything is public (no security by obscurity).
<!--deDE:
    Dieses Repository enthält die gebaute und optimierte Version meiner
    persönlichen Webseite [tsickert.com](https://tsickert.com), ausgeliefert
    über GitHub Pages. Hier wird absichtlich nichts versteckt, alles ist
    öffentlich (keine Sicherheit durch Verschleierung).
-->
<!--frFR:
    Ce dépôt contient la version construite et optimisée de mon site
    personnel [tsickert.com](https://tsickert.com), servi via GitHub Pages.
    Rien n'y est caché volontairement, tout est public (pas de sécurité par
    l'obscurité).
-->

The sources live in [website](https://github.com/thaibault/website). Do not
edit files here by hand, every deployment replaces them.
<!--deDE:
    Die Quellen liegen in [website](https://github.com/thaibault/website).
    Bearbeiten Sie die Dateien hier nicht von Hand, jede Veröffentlichung
    ersetzt sie.
-->
<!--frFR:
    Les sources se trouvent dans
    [website](https://github.com/thaibault/website). Ne modifiez pas les
    fichiers ici à la main, chaque déploiement les remplace.
-->

<!--|deDE:Funktionsweise-->
<!--|frFR:Fonctionnement-->
How it works
------------

The "Deploy website" workflow of
[website](https://github.com/thaibault/website) runs the deploy script of
[website-utilities](https://tsickert.com/website-utilities) whenever a new
version is prepared or on manual trigger. It performs these steps:
<!--deDE:
    Der Workflow "Deploy website" von
    [website](https://github.com/thaibault/website) führt das Deploy-Skript
    von [website-utilities](https://tsickert.com/website-utilities) aus,
    sobald eine neue Version vorbereitet wird oder bei manuellem Start. Es
    führt folgende Schritte aus:
-->
<!--frFR:
    Le workflow "Deploy website" de
    [website](https://github.com/thaibault/website) exécute le script de
    déploiement de [website-utilities](https://tsickert.com/website-utilities)
    dès qu'une nouvelle version est préparée ou sur déclenchement manuel. Il
    effectue les étapes suivantes:
-->

1. Pulls this repository.<!--deDE:Aktualisiert dieses Repository.--><!--frFR:Met à jour ce dépôt.-->
2. Builds the website via "yarn build".<!--deDE:Baut die Webseite mittels "yarn build".--><!--frFR:Construit le site via "yarn build".-->
3. Replaces all files here with the build result, except ".git", ".github",
   "CNAME" and this "readme.md".<!--deDE:Ersetzt alle Dateien hier durch das Build-Ergebnis, außer ".git", ".github", "CNAME" und dieser "readme.md".--><!--frFR:Remplace tous les fichiers ici par le résultat du build, sauf ".git", ".github", "CNAME" et ce "readme.md".-->
4. Commits everything as "Automatic page build update." and pushes it.<!--deDE:Committet alles als "Automatic page build update." und pusht es.--><!--frFR:Commite le tout sous "Automatic page build update." et le pousse.-->

The documentation pages of my projects, for example
[tsickert.com/web-documentation](https://tsickert.com/web-documentation), are
not part of this repository. Each project publishes them from its own
"gh-pages" branch and GitHub serves them below the same domain.
<!--deDE:
    Die Dokumentationsseiten meiner Projekte, zum Beispiel
    [tsickert.com/web-documentation](https://tsickert.com/web-documentation),
    sind nicht Teil dieses Repositorys. Jedes Projekt veröffentlicht sie aus
    seinem eigenen "gh-pages"-Branch und GitHub liefert sie unter derselben
    Domain aus.
-->
<!--frFR:
    Les pages de documentation de mes projets, par exemple
    [tsickert.com/web-documentation](https://tsickert.com/web-documentation),
    ne font pas partie de ce dépôt. Chaque projet les publie depuis sa propre
    branche "gh-pages" et GitHub les sert sous le même domaine.
-->

<!--|deDE:Inhalt-->
<!--|frFR:Contenu-->
Contents
--------

- "CNAME": Custom domain "tsickert.com" for GitHub Pages.<!--deDE:"CNAME": Eigene Domain "tsickert.com" für GitHub Pages.--><!--frFR:"CNAME": Domaine personnalisé "tsickert.com" pour GitHub Pages.-->
- "index.html", "index.css", "index.js": The built website.<!--deDE:"index.html", "index.css", "index.js": Die gebaute Webseite.--><!--frFR:"index.html", "index.css", "index.js": Le site construit.-->
- "data": Downloads such as curriculum vitae, vCard, public SSH key and audio
  files.<!--deDE:"data": Downloads wie Lebenslauf, vCard, öffentlicher SSH-Schlüssel und Audiodateien.--><!--frFR:"data": Téléchargements tels que curriculum vitae, vCard, clé SSH publique et fichiers audio.-->
- "font", "image": Fonts and images used by the website.<!--deDE:"font", "image": Von der Webseite verwendete Schriften und Bilder.--><!--frFR:"font", "image": Polices et images utilisées par le site.-->

<!--|deDE:Manuelle Veröffentlichung-->
<!--|frFR:Déploiement manuel-->
Manual deployment
-----------------

Clone this repository next to [website](https://github.com/thaibault/website)
and run the deploy script from there:
<!--deDE:
    Klonen Sie dieses Repository neben
    [website](https://github.com/thaibault/website) und starten Sie dort das
    Deploy-Skript:
-->
<!--frFR:
    Clonez ce dépôt à côté de [website](https://github.com/thaibault/website)
    et lancez le script de déploiement depuis celui-ci:
-->

```bash
git clone https://github.com/thaibault/thaibault.github.io.git
git clone https://github.com/thaibault/website.git
cd website
yarn install
GIT_PRIVATE_AUTHOR_NAME=thaibault yarn update:website
```

Instead of "GIT_PRIVATE_AUTHOR_NAME" you can point "PUBLIC_REPOSITORY_PATH"
directly to your clone of this repository.
<!--deDE:
    Statt "GIT_PRIVATE_AUTHOR_NAME" können Sie "PUBLIC_REPOSITORY_PATH" direkt
    auf Ihren Klon dieses Repositorys zeigen lassen.
-->
<!--frFR:
    Au lieu de "GIT_PRIVATE_AUTHOR_NAME", vous pouvez faire pointer
    "PUBLIC_REPOSITORY_PATH" directement vers votre clone de ce dépôt.
-->
