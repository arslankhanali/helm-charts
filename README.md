# Chart Release cr
1. In `main` branch
   1. `.github/workflows/release.yaml`: create with [default](https://github.com/marketplace/actions/helm-chart-releaser#example-workflow)
   2. `charts`: Place charts in this directory
   3. `Readme`:
2. In `gh-pages` branch
   1. `git checkout -b gh-pages`: Create Branch
   2. Select `gh-pages` as branch in [pages settings](https://github.com/arslankhanali/helm-charts/settings/pages)
   3. `touch index.yaml`: Create file and fill with sample text. sample given at the end
   4. `Readme.md`: This readme will be rendered on [page](https://arslankhanali.github.io/helm-charts/)
3. `**Automatic release**`: Each time a `new chart` is added or a version of an old chart is `changed` in `main branch`. A workflow will run and create a `new release` of the chart and packages it up. It also updates the `index.yaml` in `gh-pages branch`

## Usage

Install helm on your machine using the [official docs](https://helm.sh/docs/intro/install/)

```shell
helm repo add arslan https://arslankhanali.github.io/helm-charts/
helm repo update
helm search repo arslan

helm install llm arslan/operators

helm list 

helm uninstall llm
```


### index.yaml sample
```yml
apiVersion: v1
entries:
  blank:
  - apiVersion: v2
    created: "2023-10-05T16:14:49.678487+11:00"
    description: An empty Helm chart
    digest: 526eac5266cce78f81b84a4507b4eb8fa1e884997cc816d373524a4e46eabb56
    keywords:
    - pattern
    name: blank
    urls:
    - https://github.com/arslankhanali/helm-charts/releases/download/blank-0.0.1/blank-0.0.1.tgz
    version: 0.0.1
```