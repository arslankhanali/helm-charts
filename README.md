# Arslan's Helm Charts
Welcome to the GitHub Pages branch for My Helm Charts repository! This repository hosts Helm charts that you can use to deploy applications and services on Kubernetes clusters.

## Install Helm
[Install](https://helm.sh/docs/intro/install/) helm on your machine.  
`brew install helm`  


## Usage

To use these Helm charts, you'll need Helm installed on your local machine and access to a Kubernetes cluster. Follow these steps to get started:

1. **Add the Helm Repository**: Add the repository to Helm:

    ```bash
    helm repo add arslan https://arslankhanali.github.io/helm-charts/
    ```
2. **Repo update**: Update repo:

    ```bash
    helm repo update
    ```
3. **Search for Available Charts**: List the available charts:

    ```bash
    helm search repo arslan
    ```

4. **Install a Chart**: Install a chart on your Kubernetes cluster:
 
    ```bash
    helm install llm arslan/operators
    ```
5. **Uninstall a Chart**: Install a chart on your Kubernetes cluster:

    ```bash
    helm list 
    helm uninstall llm
    ```
6. **Customize Chart Values**: You can customize chart values by creating a `values.yaml` file and passing it to the `helm install` command with the `-f` flag.
    ```bash
    helm install llm arslan/operators -f values.yaml
    ```
For more information on Helm and how to use it, refer to the [Helm documentation](https://helm.sh/docs/).

## [Available Charts](https://github.com/arslankhanali/helm-charts/tree/main/charts)

- [operators](https://github.com/arslankhanali/helm-charts/tree/main/charts/operators): Install operators on Red Hat OpenShift
- [workbench](https://github.com/arslankhanali/helm-charts/tree/main/charts/workbench): Create a workbench in Red Hat OpenShift AI
- [rbac](https://github.com/arslankhanali/helm-charts/tree/main/charts/rbac): Create a role and rb
- [s2i](https://github.com/arslankhanali/helm-charts/tree/main/charts/s2i): Deploy a pod from a source

## Contributing

If you'd like to contribute to this repository by adding new charts, fixing bugs, or improving documentation, please fork the repository, make your changes, and submit a pull request.

## License


### Automate Chart Releases
1. For `main` branch
   1. `.github/workflows/release.yaml`: create with [default](https://github.com/marketplace/actions/helm-chart-releaser#example-workflow) values. Make sure you commit & push it.
   2. `charts`: Place charts in this directory
   3. `Readme`: You are reading this
2. For `gh-pages` branch
   1. `git checkout -b gh-pages`: Create Branch
   2. Select `gh-pages` as branch in [pages settings](https://github.com/arslankhanali/helm-charts/settings/pages)
   3. `touch index.yaml`: Create file and fill with sample text. [sample given at the end]
   4. `Readme.md`: This readme will be rendered on [page](https://arslankhanali.github.io/helm-charts/)
3. `**Automatic release**`: Each time a `new chart` is added or a version of an old chart is `changed` in `main branch`. A [workflow](https://github.com/arslankhanali/helm-charts/actions) will run and create a `new release` of the chart and packages it up. It also updates the `index.yaml` in `gh-pages branch`

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

