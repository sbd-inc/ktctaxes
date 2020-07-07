# Setup Notes

## Default starter for Gridsome

This is the project you get when you run `gridsome create new-project`.

### 1. Install Gridsome CLI tool if you don't have

`npm install --global @gridsome/cli`

### 2. Create a Gridsome project

1. `gridsome create my-gridsome-site` to install default starter
2. `cd my-gridsome-site` to open the folder
3. `gridsome develop` to start a local dev server at `http://localhost:8080`
4. Happy coding 🎉🙌

## Create from vanilla Gridsome

❯ gridsome create ktctaxes
❯ Clone https://github.com/gridsome/gridsome-starter-default.git 1.01s
❯ Update project package.json 0s
❯ Install dependencies 42.9s

  - Enter directory cd ktctaxes
  - Run gridsome develop to start local development
  - Run gridsome build to build for production

❯ cp -R gridsome-starter/.vscode ktctaxes
❯ cp gridsome-starter/.eslintrc.json ktctaxes

## Setup VSCode Workspace
### Linter
```zsh
❯ pwd
/Users/garywong/proj/anx-wp
❯ cp -R ~/Documents/sbd-wiki-js/vscode-notes/js-vscode/.vscode .
❯ cp -R ~/Documents/sbd-wiki-js/vscode-notes/js-vscode/app/.eslintrc.json .
```

### Extensions:
```zsh
code --install-extension kumar-harsh.graphql-for-vscode
code --install-extension octref.vetur
```

### User Settings(Workplace):
"vetur.grammar.customBlocks": {"page-query": "graphql", "static-query":"graphql"}

VSCode Command Palette:
Vetur: Generate grammar from 'vetur.grammer.customBlocks'

--
## Compare to my finished O'Reilly course

But if I was to get from Course material code github... 
https://github.com/reedbarger/gridsome-starter

My "finished" version is at:
https://github.com/garywong-bc/gridsome-starter

locally at: /Users/garywong/proj/gridsome-starter

## Setup GitHub Repo


Connect to separately created github private repo:
```zsh
❯ gra origin https://github.com/sbd-inc/ktctaxes.git
❯ grv
origin  https://github.com/sbd-inc/ktctaxes.git (fetch)
origin  https://github.com/sbd-inc/ktctaxes.git (push)
```

❯ gp -u origin master
Enumerating objects: 28, done.
Counting objects: 100% (28/28), done.
Delta compression using up to 8 threads
Compressing objects: 100% (25/25), done.
Writing objects: 100% (28/28), 152.77 KiB | 10.18 MiB/s, done.
Total 28 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/sbd-inc/ktctaxes.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

## GitHub Pages

As per https://gridsome.org/docs/deploy-to-github/

```bash
❯ npm i gh-pages
+ gh-pages@3.1.0
added 22 packages from 4 contributors and audited 1413 packages in 8.064s

41 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

NOTE: Changed to Public to support GitHub Pages

```zsh
❯ npm run deploy

> ktctaxes@ predeploy /Users/garywong/proj/ktctaxes
> npm run build


> ktctaxes@ build /Users/garywong/proj/ktctaxes
> gridsome build

Gridsome v0.7.17

Initializing plugins...
Load sources - 0s
Create GraphQL schema - 0.03s
Create pages and templates - 0.03s
Generate temporary code - 0.03s
Bootstrap finish - 0.62s
Compile assets - 3.13s
Execute GraphQL (3 queries) - 0s
Write out page data (3 files) - 0s
Render HTML (3 files) - 0.19s
Process files (0 files) - 0s
Process images (9 images) - 0.52s


  Done in 4.53s


> ktctaxes@ deploy /Users/garywong/proj/ktctaxes
> gh-pages -d dist

Published
```

Tested and working at https://sbd-inc.github.io/ktctaxes/
NOTE: Takes up to 20 minutes to show up.

---



vscode://vscode.github-authentication/did-authenticate?windowId=1&code=1a17b2329b0a0f602011&state=9e7b5284-2692-462f-9535-559011006982