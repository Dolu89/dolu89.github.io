---
layout: post
title: Configurer ESLint pour VS Code
categories:
- blog
---

ESLint permet d'instaurer des conventions à respecter pour écrire son code.
La configuration suivante permettra d'automatiquement formater le code en respectant ces conventions à chaque sauvegarde d'un fichier JS/TS.

Télécharger le plugin VS Code [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

Créer un fichier `.eslintrc.json` à la racine du projet pour définir les règles à respecter.
Par exemple
{% highlight json %}
{
    "extends": [
        "plugin:adonis/typescriptApp"
    ],
    "rules": {"max-len":"off"}
}
{% endhighlight %}

Créer un fichier `.vscode/settings.json`
{% highlight json %}
{
    "eslint.format.enable":  true,
    "editor.codeActionsOnSave": {
	    "source.fixAll.eslint":  true
    }
}
{% endhighlight %}
