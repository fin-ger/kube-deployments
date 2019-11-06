<h1 align="center">Welcome to my <code>kubernetes</code> deployments 👋</h1>
<p align="center">
  <a href="https://github.com/fin-ger/kube-deployments/blob/master/LICENSE">
    <img alt="GitHub" src="https://img.shields.io/github/license/fin-ger/kube-deployments.svg">
  </a>
  <a href="http://spacemacs.org">
    <img src="https://cdn.rawgit.com/syl20bnr/spacemacs/442d025779da2f62fc86c2082703697714db6514/assets/spacemacs-badge.svg" />
  </a>
  <a href="http://makeapullrequest.com">
    <img alt="PRs Welcome" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" target="_blank" />
  </a>
  <br>
  <i>A collection of my personal kubernetes deployments</i>
</p>

---

## miniserve

Run the deployment:

```
$ kubectl apply -f miniserve.yaml
```

And upload files to miniserve with

```
$ kubectl --namespace fin-static cp myfile fin-static/miniserve-<TAB>:/data/ -c miniserve-shell
```

Get an interactive shell

```
$ kubectl --namespace fin-static exec -ti -c miniserve-shell miniserve-<TAB> /bin/ash
/ # cd /data
/data # mkdir my-awesome-folder
```
