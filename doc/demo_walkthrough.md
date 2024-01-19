## demo walkthrough

1. A new Developer ("Gowtham") is joining the `DEMO` team (speech-over narrative)

2. Gowtham goes to the website and sees that the product is showing 500s. Their team lead has told them they will deploy the `carts` service to get the site fully functional.

3. The teawm dev manager adds Gowtham to the github team (in github console, add yourself to the demo-team)

4. Developer clones the Cart repo, looks over the code. Up till now, the team has only been working on this locally in minikube, so there are no deployment manifests yet.

5. Developer adds the dynamodb crossplane Table resource to each blank manifest/demo-(dev | stage | prod)/manifest.yaml. (normally a templating framework such as Helm would be used).

6. Developer pushes the change to github, the development-build workflow calls the argocd API to trigger the demo-dev anvironment deployment

7. The develop-build github workflow is triggered
   - CI steps occur, then
   - the workflow calls the argocd api to trigger a sync of the demo-dev environment of the carts application

8. Developer goes the argo console and sees that the demo-dev sync is healthy

9. Gowtham downloads the apctl cli and does `apctl login`

10. Developer gets a kubeconfig file for the nonprod environments, `apctl get kubeconfig --cluster nonprod-mkt01-aws-us-west-2 > kubeconfig`

11. Developer looks at the state of the Table and sees that it is ready.

12. Developer tags the repo with v0.1.0

13. The prod-release workflow is triggered
    - the workflow calls the argocd API to sync the demo-stage environment of the carts application
    - next, worklfow calls the argocd API to sync the demo-prod environment of the carts applicaiton

14. Developer watches in argo for those to complete

15. Developer now adds the rest of the Carts resources to the manifest files. (recur: normally would be helm, not copy/paste)

16. Developer pushes this change to git, and watches the state in ArgoCD until it is complete in demo-dev (more CI activity could occur)

17. Gowtham goes to the demo-dev instance of the website to see that the site is now up and working as expected

18. Developer tags the repo to trigger the prod-release workflow

19. Gowtham chekcs the demo-stage instance of the website, then demo-prod

20. Success




—— this approach requires net new changes

1. set applicationset to no auto-sync

2. argo-sync deployment workflow, for git push, and then for git tag
