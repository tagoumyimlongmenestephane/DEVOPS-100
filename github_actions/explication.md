CI/CD avec Github Actions

ci:
  - build
  - test(unitest, integrationtest, lint)
cd:
   - deploy


# GITHUB ACTIONS
   - definition de github actions:
     - c'est une plateforme de ci/cd nous permettant d'automatiser le build, le test et le deploiement de nos applications

   1 - ton projet doit être sur github (repot github)
      - ajouter un dossier .github/workflows
      - créer les fichiers YAML
      - ajouter des déclencheurs(schedule, event, manuel) aux actions
   2 - workflow
      - ci workflow:
      - deployement workflow
      - automate workflow
      - code scanning workflow
      - pages workflow
   3 les jobs(build, test, deploy, etc... ):
      - un workflow est composé de jobs
        - un job est composé de steps
         - un step est composé de runs
          - un run est composé de commandes 
          - une commande est composée de args

    4 - les Events:
       - push(sur quel branche)
        - push sur le master
         - declencher un workflow
       - pull request
         - declencher un workflow

    5 - runners (machine virtuelle):
       - github runners
       - docker runners
       - self hosted runners
    
    6 - actions:
      - actions are reusable
        - actions are composable
        
# CONCEPTS GITHUB ACTIONS
    
   1 - workflow:
      - c'est un processus d'automatisation de tâche
      - c'est un fichier YAML (-yml, yaml)
      - c'est composé de jobs
     - trigger:
      - push, pull_request, schedule, workflow_dispatch, manuel etc ...
   2 - les variables
     - variable workflow : env
     - variable d'environnement (dev, staging, prod)
     - variable d'organisation
     - variable du repertoire

# CONCEPTS GITHUB ACTIONS
    1 - workflow
       - c'est un processus d'automatisation de tâche (job) fichier YAML (.yml, yaml)
       - c'est composé de jobs(build, test, deploy, etc...)
       - les jobs sont composés de steps
         - les steps sont composé de commandes
         - les commandes cont composé de args

    2 - variable
       - variable du workflow :
          - env
        - variable d'environnement
           - dev, staging, prod (ici tu crèes d'abord les environnements)
        - variable d'organisation:
           - github
        - variable du repertoire
           - owner, repo
        - variable par défaut
          - github.actor
          - github.repository
          - github.sha
          - github.event_name
          - github.ref
          - github.head_ref
          - github.base_ref
          - github.server_url
          - github.api_url
          - github.graphql_url
        - creer une variable d'environnement dans le workflow
    3 - Expression:
        - ${{ github.actor }}
        - ${{ if github.ref == 'refs/heads/main }}
    4 - les workflow reutilisable
        - eviter de répeter les actions
        - permet de faire des actions communes
        - facilite la maintenance
    5 - environnement de deploiement:
        - dev, staging, prod
    6 - artefact
        - build, test, deploy 
        - c'est le output des jobs(zip, tar, logs, etc...)
    7 - cache de dépendances
       - maven, npm, pip, gradle, etc ... 
    
# SYNTHAXE DU WORKFLOW
  
   on:
     label:
       - action

* * * * *

le premier c'est les minutes (0-59)
le second c'est les heures (0-23)
le troisieme c'est les jours (0-31)
le quatrieme c'est les mois (1-12)
le cinquieme c'est les jours de la semaine (0-6 or SUN-SAT)

* * * * *



    
