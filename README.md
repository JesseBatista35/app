
-sh-4.2$
-sh-4.2$ oc get pods -n sigsj-des -l name=sigsj-frontend-rc-des
error: the server doesn't have a resource type "pods"
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc login --token=sha256~qdJdxAkPY3ioloI4o5cyvSeNB14Sz1fKueRjJwZ4LAA --server=https://api.nprd.caixa:6443
Logged into "https://api.nprd.caixa:6443" as "p585600@corp.caixa.gov.br" using the token provided.

You have access to 999 projects, the list has been suppressed. You can list all projects with 'oc projects'

Using project "sigcb-tqs".
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n sigsj-des -l name=sigsj-frontend-rc-des
NAME                             READY     STATUS    RESTARTS   AGE
sigsj-frontend-rc-des-25-gltfz   2/2       Running   0          11d
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc describe pod sigsj-frontend-rc-des-28-fxnxf -n sigsj-des | tail -30
Error from server (NotFound): pods "sigsj-frontend-rc-des-28-fxnxf" not found
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs sigsj-frontend-rc-des-28-fxnxf -n sigsj-des --previous
Error from server (NotFound): pods "sigsj-frontend-rc-des-28-fxnxf" not found
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc debug dc/sigsj-frontend-rc-des -n sigsj-des -- sh -c 'ls -la /opt/app-root/src; find /opt/app-root/src -maxdepth 3 -name "main*.js"'
Defaulting container name to sigsj-frontend-rc-des.
Use 'oc describe pod/sigsj-frontend-rc-des-debug -n sigsj-des' to see all of the containers in this pod.

Debugging with pod/sigsj-frontend-rc-des-debug, original command: <image entrypoint>
Waiting for pod to start ...
total 52
drwxr-xr-x. 1 default root    92 Oct 28 10:10 .
drwxr-xr-x. 1 default root    17 Sep 15  2021 ..
drwxr-xr-x. 1 default root    19 Sep 15  2021 .pki
-rw-r--r--. 1 default root 44156 Oct 28 10:09 3rdpartylicenses.txt
drwxr-xr-x. 4 default root  4096 Oct 28 10:09 browser
drwxr-xr-x. 2 default root     6 Oct 28 10:10 dist
drwxr-xr-x. 2 default root     6 Sep 15  2021 nginx-start
-rw-r--r--. 1 default root    18 Oct 28 10:09 prerendered-routes.json
/opt/app-root/src/browser/main-F4K75TEF.js

Removing debug pod ...
-sh-4.2$


{
  "$schema": "./node_modules/@angular/cli/lib/config/schema.json",
  "version": 1,
  "newProjectRoot": "projects",
  "projects": {
    "SIGSJ-frontend": {
      "projectType": "application",
      "schematics": {
        "@schematics/angular:component": {
          "style": "scss"
        }
      },
      "root": "",
      "sourceRoot": "src",
      "prefix": "app",
      "architect": {
        "build": {
          "builder": "@angular-devkit/build-angular:application",
          "options": {
            "outputPath": "dist/sigsj-frontend",
            "index": "src/index.html",
            "browser": "src/main.ts",
            "polyfills": [
              "zone.js"
            ],
            "tsConfig": "tsconfig.app.json",
            "inlineStyleLanguage": "scss",
            "assets": [
              {
                "glob": "**/*",
                "input": "public"
              }
            ],            
            "scripts": [],
            "styles": [
              "node_modules/sidsc-components/styles/main.scss",
              "node_modules/@fortawesome/fontawesome-free/css/all.min.css",
              "src/styles.scss"
            ]
          },
          "configurations": {
            "production": {
              "budgets": [
                {
                  "type": "initial",
                  "maximumWarning": "2MB",
                  "maximumError": "3MB"
                },
                {
                  "type": "anyComponentStyle",
                  "maximumWarning": "4kB",
                  "maximumError": "8kB"
                }
              ],
              "outputHashing": "all"
            },
            "development": {
              "optimization": false,
              "extractLicenses": false,
              "sourceMap": true
            }
          },
          "defaultConfiguration": "production"
        },
        "serve": {
          "builder": "@angular-devkit/build-angular:dev-server",
          "configurations": {
            "production": {
              "buildTarget": "SIGSJ-frontend:build:production"
            },
            "development": {
              "buildTarget": "SIGSJ-frontend:build:development"
            }
          },
          "defaultConfiguration": "development"
        },
        "extract-i18n": {
          "builder": "@angular-devkit/build-angular:extract-i18n"
        },
        "test": {
          "builder": "@angular-devkit/build-angular:karma",
          "options": {
            "polyfills": [
              "zone.js",
              "zone.js/testing"
            ],
            "tsConfig": "tsconfig.spec.json",
            "inlineStyleLanguage": "scss",
            "assets": [
              {
                "glob": "**/*",
                "input": "public"
              }
            ],
            "styles": [
              "node_modules/@fortawesome/fontawesome-free/css/all.min.css",
              "src/styles.scss"
            ],
            "scripts": [],
            "karmaConfig": "karma.conf.js"
          }
        }
      }
    }
  },
  "cli": {
    "analytics": "ca8e8c6c-1daa-43f7-b9cc-561786380db6"
  }
}


Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Files
/

SIGSJ-frontend
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
SIGSJ-frontend

.s2i
.vscode
docs
e2e
playwright-report
public
src
.editorconfig
.gitignore
.npmrc
angular.json
COMPONENTES_SIGSJ_MANUAL.md
gitflow
karma.conf.js
package-lock.json
package.json
playwright.config.ts
README.md
tsconfig.app.json
tsconfig.json
tsconfig.spec.json

novolayout-ds

/
angular.json
angular.json

Edit

Contents
History
Compare
Blame

1234567891011121314151617181920212223242526272829303132333435363738394041424344
{
  "$schema": "./node_modules/@angular/cli/lib/config/schema.json",
  "version": 1,
  "newProjectRoot": "projects",
  "projects": {
    "SIGSJ-frontend": {
      "projectType": "application",
      "schematics": {
        "@schematics/angular:component": {
          "style": "scss"
…          }
        }
      }
    }
  },
  "cli": {
    "analytics": "ca8e8c6c-1daa-43f7-b9cc-561786380db6"
  }
}


