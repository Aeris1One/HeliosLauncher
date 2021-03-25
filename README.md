<p align="center"><img src="./app/assets/images/SealCircle.png" width="150px" height="150px" alt="aventium softworks"></p>

<h1 align="center">Terebros Launcher</h1>

[<p align="center"><img src="https://img.shields.io/travis/Terebros-MC/TerebrosLauncher.svg?style=for-the-badge" alt="travis">](https://travis-ci.com/Terebros-MC/HeliosLauncher) [<img src="https://img.shields.io/github/downloads/Terebros-MC/HeliosLauncher/total.svg?style=for-the-badge" alt="downloads">](https://github.com/Terebros-MC/HeliosLauncher/releases)</p>

<p align="center">Rejoignez Terebros sans vous soucier de Java, Forge ou même des mods.</p>

![Screenshot 1](https://i.imgur.com/6o7SmH6.png)
![Screenshot 2](https://i.imgur.com/x3B34n1.png)

## Features

* 🔒 Gestion de comptes personnels TerebrAuth.
  * Ajoutez plusieurs comptes et basculez entre eux.
  * Les comptes sont gérés par TerebrAuth pour vous fournir une sécurité accrue.
* 📂 Gestion performante des données
  * Recevez les mises à jour dès que nous les publions.
  * Validation des fichiers avant chaque lancement : les fichiers corrompus seront retéléchargés.
* ☕ **Validation automatique de Java.**
  * Si vous avez une version incompatible de Java nous installerons la bonne *pour vous*.
  * Vous n'avez pas besoin de Java pour utiliser le launcher.
* 📰 Nouveautés directement dans le launcher.
* ⚙️ Gestion intuitive des paramètres de jeu et de Java.
* Supporte tous nos serveurs.
  * Changez de configuration en quelques clics.
  * Affichage du nombre de joueurs sur chaque serveur.
* Mises à jour automatiques. Vous avez bien lu : le launcher se met à jour seul.

Cette liste n'est pas complète ! Téléchargez et jetez un oeil par vous-même !

#### Besoin d'aide ? [Allez voir le wiki][wiki]

#### Vous aimez le projet ? Laissez une ⭐ sur ce dépot !

## Téléchargements

Vous pouvez télécharger depuis [GitHub Releases](https://github.com/Aeris1One/TerebrosLauncher/releases)

#### Latest Release

[![](https://img.shields.io/github/release/Aeris1One/TerebrosLauncher.svg?style=flat-square)](https://github.com/Aeris1One/TerebrosLauncher/releases/latest)

#### Latest Pre-Release
[![](https://img.shields.io/github/release/Aeris1One/TerebrosLauncher/all.svg?style=flat-square)](https://github.com/Aeris1One/TerebrosLauncher/releases)

**Supported Platforms**
Si vous téléchargez depuis [Github Releases](https://github.com/Aeris1One/TerebrosLauncher/releases), selectionnez l'installeur pour votre système.

| Platform | File |
| -------- | ---- |
| Windows x64 | `terebroslauncher-setup-VERSION.exe` |
| macOS | `terebroslauncher-VERSION.dmg` |
| Linux x64 | `terebroslauncher-VERSION-x86_64.AppImage` |


## Console

Pour ouvrir la console, utilisez la combinaison suivante :

```console
ctrl + shift + i
```
Assurez-vous d'être dans l'onglet Console.
Ne copiez-coller aucun code sans être vraiment sûr de ce qu'il fait : vous pourriez exposer des informations sensibles !

#### Export Output to a File

Si vous voulez exporter le contenu de la console, il suffit de faire clic droit puis **Save as..**

![console example](https://i.imgur.com/T5e73jP.png)


## Developpement

<<<<<<< HEAD
### Démarrer
=======
This section details the setup of a basic developmentment environment.

### Getting Started
>>>>>>> 48d0c9e5490ad67f58aa88d2920bab9d3af46128

**Dépendances**

* [Node.js][nodejs] v14

---

**Cloner et installer les dépendances additionnelles**

```console
> git clone https://github.com/Aeris1One/TerebrosLauncher.git
> cd TerebrosLauncher
> npm install
```

---

**Lancer l'application**

```console
> npm start
```

---

**Construire les installeurs**

Pour votre système.

```console
> npm run dist
```

Pour un autre système.

| Platform    | Command              |
| ----------- | -------------------- |
| Windows x64 | `npm run dist:win`   |
| macOS       | `npm run dist:mac`   |
| Linux x64   | `npm run dist:linux` |

<<<<<<< HEAD
Vous ne pouvez pas construire les installeurs pour MacOS sur Windows et Linux et ne pouvez pas créer d'installateurs pour Windows et Linux depuis MacOS
=======
Builds for macOS may not work on Windows/Linux and vice-versa.

---

### Visual Studio Code

All development of the launcher should be done using [Visual Studio Code][vscode].

Paste the following into `.vscode/launch.json`

```JSON
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Main Process",
      "type": "node",
      "request": "launch",
      "cwd": "${workspaceFolder}",
      "program": "${workspaceFolder}/node_modules/electron/cli.js",
      "args" : ["."],
      "outputCapture": "std"
    },
    {
      "name": "Debug Renderer Process",
      "type": "chrome",
      "request": "launch",
      "runtimeExecutable": "${workspaceFolder}/node_modules/.bin/electron",
      "windows": {
        "runtimeExecutable": "${workspaceFolder}/node_modules/.bin/electron.cmd"
      },
      "runtimeArgs": [
        "${workspaceFolder}/.",
        "--remote-debugging-port=9222"
      ],
      "webRoot": "${workspaceFolder}"
    }
  ]
}
```

This adds two debug configurations.

#### Debug Main Process

This allows you to debug Electron's [main process][mainprocess]. You can debug scripts in the [renderer process][rendererprocess] by opening the DevTools Window.

#### Debug Renderer Process

This allows you to debug Electron's [renderer process][rendererprocess]. This requires you to install the [Debugger for Chrome][chromedebugger] extension.

Note that you **cannot** open the DevTools window while using this debug configuration. Chromium only allows one debugger, opening another will crash the program.

---

### Note on Third-Party Usage

You may use this software in your own project so long as the following conditions are met.

* Credit is expressly given to the original authors (Daniel Scalzi).
  * Include a link to the original source on the launcher's About page.
  * Credit the authors and provide a link to the original source in any publications or download pages.
* The source code remain **public** as a fork of this repository.

We reserve the right to update these conditions at any time, please check back periodically.

---

## Resources

* [Wiki][wiki]
* [Nebula (Create Distribution.json)][nebula]
* [v2 Rewrite Branch (WIP)][v2branch]

The best way to contact the developers is on Discord.

[![discord](https://discordapp.com/api/guilds/211524927831015424/embed.png?style=banner3)][discord]
>>>>>>> 48d0c9e5490ad67f58aa88d2920bab9d3af46128

---

### À plus en jeu ;)


[nodejs]: https://nodejs.org/en/ 'Node.js'
[vscode]: https://code.visualstudio.com/ 'Visual Studio Code'
[mainprocess]: https://electronjs.org/docs/tutorial/application-architecture#main-and-renderer-processes 'Main Process'
[rendererprocess]: https://electronjs.org/docs/tutorial/application-architecture#main-and-renderer-processes 'Renderer Process'
[chromedebugger]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome 'Debugger for Chrome'
[discord]: https://discord.gg/zNWUXdt 'Discord'
[wiki]: https://github.com/dscalzi/HeliosLauncher/wiki 'wiki'
[nebula]: https://github.com/dscalzi/Nebula 'dscalzi/Nebula'
[v2branch]: https://github.com/dscalzi/HeliosLauncher/tree/ts-refactor 'v2 branch'
