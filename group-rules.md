# Group rules:

## Stand up:

Group Rules
Sprint = 1 week

## Two standups per day:

One after Switchfully stand-up
One after secret

## Ownership

Ownership of stories will be defined after reading them.
General rule of thumb, one group does one story, check in afterwards.

Pairing/repairing -> one change per day foreseen, after the second stand-up. On s’arrange

Code review: One group creates a part of code, the other group reviews it. TODO: to be decided later on if this process
needs adjusting/changes, we use AI.

When we take a story, that means it needs to be completed in its entirety (so endpoints, tests, … too)

## Kanban steps

- Backlog: Once we are all clear on what a story means, no further questions need to be asked to the functional analyst.
- Sprint : Stories selected for the sprint
- In progress: Once a story has been assigned to a group to work on.
- To Tests : The feature needs to have tests implemented.
- In review: A team actually picks up a story to review. The reviewer merges the branch into main.
- Done: Review is done.

## Commit conventions

- feat: Adds a new feature to the application (correlates with MINOR semantic version).
- fix: Resolves a bug in the code (correlates with PATCH semantic version).
- docs: Documentation-only changes.
- style: Formatting, missing semi-colons, or whitespace changes (no logic change).
- refactor: Code restructuring that neither fixes a bug nor adds a feature.
- perf: Code changes that improve performance.
- test: Adding missing tests or correcting existing tests.
- chore: Maintenance tasks, build process changes, or package
  Example : feat(name_of_the_story) : Describe briefly the commit in present tense

## Some Git commands

How to create a new branch and move to it in one command :
`git checkout -b name_of_new_branch`
How to just move to another branch:
`git checkout name_of_branch`
How to merge (from the branch that’s receiving)
`git merge`

## Structure
- Backend: by features ->  
exemple:
```
|_register
    |_controller
    |_service
    |_mapper
    |_dtos
       |_registerRequestDto
       |_registerResponseDto 
       |_registerDetailsResponseDto
``` 
Frontend: Core et pages separated, core by layer et pages by feature
exemple:
```
|_core
   |_services // calls the backend and changes uses the mapper
   |_register.service.ts
   |_controllers // authorizations
       |_register.controller.ts
   |_dtos
      |_requests
      |_responses
   |_mappers
|_ shared // Components that are used in multiple features
      |_forms
|_pages // the visible pages for the users
   |_auth
      |_register // = register page
         |_register.component.ts
         |_register.component.html
         |_register.component.css
         |_register.component.spec.ts
      |_login … // = login page
   |_auth.routes.ts
```
## DOSprint
 - story reviewed
 -  La story a des critères d'acceptation testables
 - Les questions métier ont reçu une réponse de l'analyste
 - Les sous-tâches techniques sont listées dans l'issue
## DODone
- Tous les critères d'acceptation sont couverts par des tests (unitaires + intégration sur H2)
- La migration Flyway est incluse si le schéma change
- DTOs de requête et de réponse séparés ; aucune entité JPA exposée par l'API
- Erreurs gérées (400 / 404 / 403) et loguées
- Endpoint visible et documenté dans Swagger UI
- PR relue et approuvée par l'autre paire
- Pipeline GitHub Actions vert sur main après merge
- Endpoint testé manuellement (Swagger ou fichier .http / Postman)
- Idem frontend

## Splitting the work

-

## Questions for the analysts

-

## Techno

Css : Bootstrap

Github:
Repo:
https://github.com/nomoli98/2026_Switchfully_final_project_lms

Project:
https://github.com/users/nomoli98/projects/13/views/1